FROM golang:1.13.7-alpine3.11 AS build
RUN apk --no-cache add bash g++ openssl git
RUN go get -u github.com/mitchellh/gox

ENV SWAGGER_VERSION=v0.22.0

ENV REPO="github.com/go-swagger/go-swagger/cmd/swagger"
RUN go get -u "${REPO}"
WORKDIR /go/src/github.com/go-swagger/go-swagger
RUN git checkout "${SWAGGER_VERSION}"
RUN gox --osarch "linux/amd64" -output /swagger \
      -ldflags "-s -w -X ${REPO}/commands.Version=${SWAGGER_VERSION} -X ${REPO}/commands.Commit=$(git rev-parse --short HEAD)" "${REPO}"

FROM alpine:3.11
COPY --from=build /swagger /usr/bin/swagger
ENV GOPATH=/go
WORKDIR /go/src
ENTRYPOINT ["swagger"]
CMD ["-h"]
