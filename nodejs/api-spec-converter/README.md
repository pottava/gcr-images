# LucyBot-Inc/api-spec-converter

Convert API descriptions between popular formats such as OpenAPI (fka Swagger), RAML, API Blueprint, WADL, etc.

## Supported tags

- 2.11 ([nodejs/api-spec-converter/versions/2.11/Dockerfile](https://github.com/pottava/gcr-images/blob/master/nodejs/api-spec-converter/versions/2.11/Dockerfile))

## Usage

```console
$ docker run --rm -t -v $(pwd):/work \
    pottava/gcr-images/api-spec-converter:2.11 \
    --from=openapi_3 --to=swagger_2 --syntax=yaml spec.yaml > swagger-v2.yml
```
