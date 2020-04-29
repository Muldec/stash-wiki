There is a GraphQL API which allows to do things automatically.
All http requests have to go to ``http://IP:PORT/graphql``

### Scan for new files
Request: `HTTP-POST`

Payload (set **useFileMetadata** to ```true``` or ```false``` if you want to get metadata from the media file ):
```json
{
  "query": "mutation { metadataScan ( input: { useFileMetadata: true } ) } "
}
```
_Example using curl (use of **-u username:password** is needed only if you added a password to the configuration )_

`curl -u username:password -X POST -H "Content-Type: application/json" --data '{ "query": " mutation { metadataScan (input: { useFileMetadata: false} ) }" }' localhost:9998/graphql`

### Generate content

Request: `HTTP-POST`

Payload (set desired content to generate **sprites**,**previews**,**markers**,**transcodes** to ```true``` or ```false```):
```json
{
  "query": "{ metadataGenerate ( input : { sprites: true previews: false markers:false transcodes:false } ) }" 
}
```
_Example using curl_

`curl -X POST -H "Content-Type: application/json" --data '{ "query": "{ metadataGenerate ( input : { sprites: false previews: true markers:false transcodes:false } ) }" }' localhost:9998/graphql`

### Get Studios

Request: `HTTP-POST`

Payload ( must be at least one of ```id``` ```checksum``` ```url``` ```name``` ```image_path``` ```scene_count``` ):
```json
{
  "query": "{ allStudios { id checksum url name image_path scene_count } }" 
}
```
_Example using curl_

`curl -X POST -H "Content-Type: application/json" --data '{ "query": "{ allStudios { name url scene_count} }" }' localhost:9998/graphql`

### Scrape perfomer attributes from Freeones

Request: `HTTP-POST`

Payload (
* ```$performer name``` is the name of the Performer you are scraping for
* return values must be at least one of ```name``` ```url``` ```twitter``` ```instagram``` ```birthdate``` ```ethnicity``` ```country``` ```eye_color``` ```height``` ```measurements``` ```fake_tits``` ```career_length``` ```tattoos``` ```piercings``` ```aliases```

):
```json
{
  "query": "{ scrapeFreeones(performer_name: $performer_name) { name url twitter instagram birthdate ethnicity country eye_color height measurements fake_tits career_length tattoos piercings aliases } }" 
}
```
1. Caution is needed when used in a script.Always set a waiting/sleep period between calls to avoid getting blacklisted by Freeones
2. Due to way it's used in Stash and to work reliably it requires the prior use of **scrapeFreeonesPerfomerList** (described beneath) to make sure the name of the performer exists in the list returned and thus in the Freeones db


_Example using curl_

`curl -u username:password -X POST -H "Content-Type: application/json" --data '{ "query": "{ scrapeFreeones ( performer_name : \"Abella Danger\" ) { name height birthdate} }" }' localhost:9998/graphql`

### Get list of perfomer names that match a name or alias from Freeones

Request: `HTTP-POST`

Payload ( $q is the name or alias (or partial name , alias) of the performer you are looking for
):
```json
{
  "query": "{ scrapeFreeonesPerformerList(query: $q) }" 
}
```
1. Caution is needed when used in a script.Always set a waiting/sleep period between calls to avoid getting blacklisted by Freeones

_Example using curl_


`curl -u username:password -X POST -H "Content-Type: application/json" --data '{ "query": "{ scrapeFreeonesPerformerList (query: \"bella\" ) }" }' localhost:9998/graphql`
