There is a GraphQL API which allows to do things automatically.
All http requests have to go to ``http://IP:PORT/graphql``


### Scan for new files
Request: `HTTP-POST`

Payload:
```json
{
  "query": "{ metadataScan }"
}
```

### Generate previews

Request: `HTTP-POST`

Payload (set desired previews to ```true``` or ```false```):
```json
{
  "query": "{ metadataGenerate ( input : { sprites: true previews: false markers:false transcodes:false } ) }" 
}
```

