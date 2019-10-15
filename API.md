There is a GraphQL API which allows to do things automatically.
All http requests have to go to ``http://IP:PORT/graphql``


### Scan for new files
Request: `HTTP-POST`

Payload (set nameFromMetadata to ```true``` or ```false``` if you want to get metadata from the media file ):
```json
{
  "query": "{ metadataScan ( input: { nameFromMetadata: true } ) } "
}
```
_Example using curl_

`curl -X POST -H "Content-Type: application/json" --data '{ "query": "{ metadataScan (input: { nameFromMetadata: false} ) }" }' localhost:9998/graphql`

### Generate previews

Request: `HTTP-POST`

Payload (set desired files to generate (sprites,previews,markers,transcodes) to ```true``` or ```false```):
```json
{
  "query": "{ metadataGenerate ( input : { sprites: true previews: false markers:false transcodes:false } ) }" 
}
```
_Example using curl_

`curl -X POST -H "Content-Type: application/json" --data '{ "query": "{ metadataGenerate ( input : { sprites: false previews: true markers:false transcodes:false } ) }" }' localhost:9998/graphql`
