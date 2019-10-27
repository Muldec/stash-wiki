There is a GraphQL API which allows to do things automatically.
All http requests have to go to ``http://IP:PORT/graphql``

### Scan for new files
Request: `HTTP-POST`

Payload (set **nameFromMetadata** to ```true``` or ```false``` if you want to get metadata from the media file ):
```json
{
  "query": "{ metadataScan ( input: { nameFromMetadata: true } ) } "
}
```
_Example using curl (use of **-u username:password** is needed only if you added a password to the configuration )_

`curl -u username:password -X POST -H "Content-Type: application/json" --data '{ "query": "{ metadataScan (input: { nameFromMetadata: false} ) }" }' localhost:9998/graphql`

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