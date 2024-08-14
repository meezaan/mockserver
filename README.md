# Run

```
docker run -p 1080:1080 docker.io/mockserver/mockserver:5.15.0
```

# Feed the MockServer an OpenAPI Spec

```
curl -v -X PUT "http://localhost:1080/mockserver/openapi" -d @specs/oapi.ex.json
curl -v -X PUT "http://localhost:1080/mockserver/openapi" -d @specs/one.json
```

# Use the Mock

```
curl -v -H 'X-Request-ID: e0866d3c-3a21-4ad6-aaf7-ca97a377e2b2' http://localhost:1080/v1/pets/1
curl -v "http://localhost:1080/distance/v1/address/London,UK/Birmingham,UK?apikey=myreallyspecialapikey"
```
