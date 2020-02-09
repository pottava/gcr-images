# ShellCheck

http://www.shellcheck.net

## Supported tags and respective `Dockerfile` links

・0.x ([haskell/shellcheck/versions/0.x/Dockerfile](https://github.com/pottava/gcr-images/blob/master/haskell/shellcheck/versions/0.x/Dockerfile))  

## Usage

```
$ docker run --rm -it -v $(pwd):/work -e IGNORE_PATH=/vendor/ \
    pottava/gcr-images/shellcheck:0.x
```
