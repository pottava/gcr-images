# go-swagger

[Swagger 2.0 implementation for go](ghttps://github.com/go-swagger/go-swagger/blob/master/README.md)

## Supported tags

- 0.22 ([go/go-swagger/versions/0.22/Dockerfile](https://github.com/pottava/gcr-images/blob/master/go/go-swagger/versions/0.22/Dockerfile))

## Usage

### Validate a OpenAPI v2 spec file

```
$ docker run --rm -v $(pwd):/go/src \
    pottava/gcr-images/go-swagger:0.22 \
    validate ./swagger.yml
```

### Generate source code

```
$ docker run --rm -v $GOPATH/src:/go/src \
    -w /go/src/github.com/your-account/project \
    pottava/gcr-images/go-swagger:0.22 \
    generate server -A sample -f swagger.yml
```
