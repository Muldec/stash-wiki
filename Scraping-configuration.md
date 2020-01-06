As of develop release 5078402, custom scraping of performer and scene details is now supported.

By default, Stash looks for scraper configurations in the `scrapers` sub-directory of the directory where the stash `config.yml` is read. This will either be the `$HOME/.stash` directory or the current working directory.

Custom scrapers are added by adding configuration yaml files to the `scrapers` directory. The configuration file looks like the following:

# Basic scraper configuration file structure

```
name: <site>
performerByName:
  <single scraper config>
performerByFragment:
  <single scraper config>
performerByURL:
  <multiple scraper URL configs>
sceneByFragment:
  <single scraper config>
sceneByURL:
  <multiple scraper URL configs>
<other configurations>
```

`name` is mandatory, all other top-level fields are optional. The inclusion of each top-level field determines what capabilities the scraper has.

A scraper configuration in any of the top-level fields must at least have an `action` field. The other fields are required based on the value of the `action` field.

The scraping types and their required fields are outlined in the following table:

| Behaviour | Required configuration |
|-----------|------------------------|
| Scraper in `Scrape...` dropdown button in Performer Edit page | Valid `performerByName` and `performerByFragment` configurations. |
| Scrape performer from URL | Valid `performerByURL` configuration with matching URL. |
| Scraper in `Scrape...` dropdown button in Scene Edit page | Valid `sceneByFragment` configuration. |
| Scrape scene from URL | Valid `sceneByURL` configuration with matching URL. |

URL-based scraping accepts multiple scrape configurations, and each configuration requires a `url` field. stash iterates through these configurations, attempting to match the entered URL against the `url` fields in the configuration. It executes the first scraping configuration where the entered URL contains the value of the `url` field. 

# Scraper Actions

## Script

Executes a script to perform the scrape. The `script` field is required for this action and accepts a list of string arguments. For example:

```
action: script
script:
  - python
  - iafdScrape.py
  - query
```

This configuration would execute `python iafdScrape.py query`.

Stash sends data to the script process's `stdin` stream and expects the output to be streamed to the `stdout` stream. Any errors and progress messages should be output to `stderr`.

The script is sent input and expects output based on the scraping type, as detailed in the following table:

| Scrape type | Input | Output |
|-------------|-------|--------|
| `performerByName` | `{"name": "<performer query string>"}` | Array of JSON-encoded performer fragments (including at least `name`) |
| `performerByFragment` | JSON-encoded performer fragment | JSON-encoded performer fragment |
| `performerByURL` | `{"url": "<url>"}` | JSON-encoded performer fragment |
| `sceneByFragment` | JSON-encoded scene fragment | JSON-encoded scene fragment |
| `sceneByURL` | `{"url": "<url>"}` | JSON-encoded scene fragment |

For `performerByName`, only `name` is required in the returned performer fragments. One entire object is sent back to `performerByFragment` to scrape a specific performer, so the other fields may be included to assist in scraping a performer. For example, the `url` field may be filled in for the specific performer page, then `performerByFragment` can extract by using its value.

As an example, the following python code snippet can be used to scrape a performer:

```
import json
import sys
import string

def readJSONInput():
	input = sys.stdin.read()
	return json.loads(input)

def searchPerformer(name):
    # perform scraping here - using name for the query

    # fill in the output
    ret = []
    
    # example shown for a single found performer 
    p = {}
    p['name'] = "some name"
    p['url'] = "performer url"
    ret.append(p)
    
    return ret

def scrapePerformer(input):
    ret = []
    # get the url from the input
    url = input['url']
    return scrapePerformerURL(url)

def debugPrint(t):
    sys.stderr.write(t + "\n")

def scrapePerformerURL(url):
    debugPrint("Reading url...")
    debugPrint("Parsing html...")
    
    # parse html

    # fill in performer details - single object
    ret = {}

    ret['name'] = "fred"
    ret['aliases'] = "freddy"
    ret['ethnicity'] = ""
    # and so on

    return ret

# read the input 
i = readJSONInput()

if sys.argv[1] == "query":
    ret = searchPerformer(i['name'])
    print(json.dumps(ret))
elif sys.argv[1] == "scrape":
    ret = scrapePerformer(i)
    print(json.dumps(ret))
elif sys.argv[1] == "scrapeURL":
    ret = scrapePerformerURL(i['url'])
    print(json.dumps(ret))
```

## scrapeXPath

This action scrapes a web page using an xpath configuration to parse. This action is valid for `performerByURL` and `sceneByURL` only.

This action requires that the top-level `xPathScrapers` configuration is populated. The `scraper` field is required and must match the name of a scraper name configured in `xPathScrapers`. For example:

```
sceneByURL:
- action: scrapeXPath
  url: 
    - pornhub.com/view_video.php
  scraper: sceneScraper
```

The above configuration requires that `sceneScraper` exists in the `xPathScrapers` configuration.

### XPath scrapers configuration

The top-level `xPathScrapers` field contains xpath scraping configurations, freely named. The scraping configuration may contain a `common` field, and must contain `performer` or `scene` depending on the scraping type it is configured for. 

Within the `performer`/`scene` field are key/value pairs corresponding to the golang fields on the performer/scene object. These fields are case-sensitive. The values of these are xpaths that tell the system where to get the value of the field from. For example:

```
performer:
  Name: //h1[@itemprop="name"]
```

This will set the `Name` attribute of the returned performer to the text content of the element that matches `<h1 itemprop="name">...`.

The `common` field is used to configure xpath fragments that can be referenced in the xpath strings. These are key-value pairs where the key is the string to reference the fragment, and the value is the string that the fragment will be replaced with. For example:

```
common:
  $infoPiece: //div[@class="infoPiece"]/span
performer:
  Measurements: $infoPiece[text() = 'Measurements:']/../span[@class="smallInfo"]  
```

The `Measurements` xpath string will replace `$infoPiece` with `//div[@class="infoPiece"]/span`, resulting in: `//div[@class="infoPiece"]/span[text() = 'Measurements:']/../span[@class="smallInfo"]`.

A minimal performer and scene xpath scraper is shown as an example below:

```
name: Pornhub
performerByURL:
  - action: scrapeXPath
    url: 
      - pornhub.com
    scraper: performerScraper
sceneByURL:
  - action: scrapeXPath
    url: 
      - pornhub.com/view_video.php
    scraper: sceneScraper
xPathScrapers:
  performerScraper:
    common:
      $infoPiece: //div[@class="infoPiece"]/span
    performer:
      Name: //h1[@itemprop="name"]
      Measurements: $infoPiece[text() = 'Measurements:']/../span[@class="smallInfo"]
  sceneScraper:
    common:
      $performer: //div[@class="pornstarsWrapper"]/a[@data-mxptype="Pornstar"]
      $studio: //div[@data-type="channel"]/a
    scene:
      Title: //div[@id="main-container"]/@data-video-title
      Tags: 
        Name: //div[@class="categoriesWrapper"]//a[not(@class="add-btn-small ")]
      Performers:
        Name: $performer/@data-mxptext
        URL: $performer/@href
      Studio:
        Name: $studio
        URL: $studio/@href    
```

## Stash

A different stash server can be configured as a scraping source. This action applies only to `performerByName`, `performerByFragment`, and `sceneByFragment` types. This action requires that the top-level `stashServer` field is configured.

`stashServer` contains a single `url` field for the remote stash server. The username and password can be embedded in this string using `username:password@host`.

An example stash scrape configuration is below:

```
name: stash
performerByName:
  action: stash
performerByFragment:
  action: stash
sceneByFragment:
  - action: stash
stashServer:
  url: http://stashserver.com:9999
```
