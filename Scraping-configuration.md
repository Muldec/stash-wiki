As of develop release 1724706, custom scraping of performer details is now supported.

By default, Stash looks for scraper configurations in the `scrapers` sub-directory of the directory where the stash `config.yml` is read. This will either be the `$HOME/.stash` directory or the current working directory.

Custom scrapers are added by adding configuration json files to the `scrapers` directory. The configuration file looks like the following:

```
{
 "name": "<site>",
 "type": "PERFORMER",
 "method": "SCRIPT",
 "urls": ["site.com"],	
 "get_performer_names": ["python", "iafdScrape.py", "query"],
 "get_performer": ["python", "iafdScrape.py", "scrape"],
 "get_performer_url": ["python", "iafdScrape.py", "scrapeURL"]
}
```

An explanation of the fields is shown below:

| Field  | Explanation |
|--------|-------------|
| `name`   | This is displayed in the `Scrape...` dropdown button. |
| `type`    | Must be `PERFORMER` currently. |
| `method` | Must be `SCRIPT` currently. |
| `urls`   | A list of url fragments. Used to match URL when parsing from URL. |
| `get_performer_names` | Script to run to perform a query from an input performer name. Used in the scrape performer dialog. |
| `get_performer` | Script to run to scrape a specific performer's details. |
| `get_performer_url` | Script to run to scrape performer details from a provided URL. |

Stash sends data to the script process's `stdin` stream and expects the output to be streamed to the `stdout` stream. Any errors and progress messages should be output to `stderr`.

The `get_performer` and `get_performer_names` fields must be present in order for the scraper to appear in the `Scrape...` dropdown button. The `urls` and `get_performer_url` fields must be present for URL parsing to be enabled.

The `get_performer_names` script is sent the following information to its `stdin` stream:
```
{"name": "<performer query string>"}
```

Stash expects the `get_performer_names` script to return data in the following format:
```
[
 {
  "name": "<string>",
  "url": "<string>",
  "twitter": "<string>",
  "instagram": "<string>",
  "birthdate": "<string>",
  "ethnicity": "<string>",
  "country": "<string>",
  "eye_color": "<string>",
  "height": "<string>",
  "measurements": "<string>",
  "fake_tits": "<string>",
  "career_length": "<string>",
  "tattoos": "<string>",
  "piercings": "<string>",
  "aliases": "<string>"
 },
 ...
]
```

Only `name` is required. One entire object is sent back to `get_performer` to scrape a specific performer, so the other fields may be included to assist in scraping a performer. For example, the `url` field may be filled in for the specific performer page, then `get_performer` can extract by using its value.

`get_performer` and `get_performer_url` both return a single instance of the object above, not an array.

The `get_performer_url` script is sent the following information to its `stdin` stream:
```
{"url": "<url>"}
```

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
