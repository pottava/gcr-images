# yq

[Command-line YAML/XML processor - jq wrapper for YAML and XML documents](https://yq.readthedocs.io/en/latest/)

## Supported tags

- 2.10 ([python/yq/versions/2.10/Dockerfile](https://github.com/pottava/gcr-images/blob/master/python/yq/versions/2.10/Dockerfile))

## Usage

### Filtering like jq

```console
$ docker run --rm -t -v $(pwd):/work \
    pottava/gcr-images/yq:2.10 \
    sh -c "cat sample.yaml | yq -y '.key'"
```

### Converting JSON to YAML

```console
$ docker run --rm -t -v $(pwd):/work \
    pottava/gcr-images/yq:2.10 \
    sh -c "cat sample.json | yq -y ." > sample.yaml
```
