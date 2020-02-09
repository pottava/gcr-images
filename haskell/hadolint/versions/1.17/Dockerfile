# Haskell Dockerfile Linter v1.17
# @see https://github.com/hadolint/hadolint

FROM alpine:3.11

ENV HADOLINT_VERSION='v1.17.5' \
    DOCKERFILE_NAME='Dockerfile'

RUN apk --no-cache --virtual=build-deps add curl bash \
    && curl --location --silent -o /usr/bin/hadolint \
       "https://github.com/hadolint/hadolint/releases/download/${HADOLINT_VERSION}/hadolint-Linux-x86_64" \
    && chmod +x /usr/bin/hadolint \
    && apk del --purge -r build-deps

WORKDIR /work

COPY entrypoint.sh /
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
