## Search API

Copied from source article: <https://outcrawl.com/go-elastic-search-service>


```
Upload a couple of fake documents, for example, documents found inside fake-data.json file.

$ curl -X POST http://localhost:8080/documents -d @fake-data.json -H "Content-Type: application/json"
Try it out.

$ curl http://localhost:8080/search?query=exercitation+est+officia
{
  "time": "42",
  "hits": "43",
  "documents": [{
      "title": "Exercitation est officia fugiat labore deserunt est id voluptate magna.",
      "created_at": "2018-03-21T15:22:48.7830606Z",
      "content": "..."
    },
    // ...
  ]
}
```

### Docker

#### Docker up

`docker-compose up -d --build`

```
-d        # Detached mode
--build   # Build images before starting containers
```

#### Stop container

`docker ps`
`docker stop search_api`
`docker stop elasticsearch`


