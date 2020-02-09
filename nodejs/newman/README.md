# Newman

[The cli companion for postman](https://www.npmjs.com/package/newman)

## Supported tags

- 4.5 ([nodejs/newman/versions/4.5/Dockerfile](https://github.com/pottava/gcr-images/blob/master/nodejs/newman/versions/4.5/Dockerfile))

## Usage

```console
$ docker run --rm -it -v $(pwd):/work \
    pottava/gcr-images/newman:4.5 \
    run collection.json
```
