FROM node:12.15.0-alpine3.11

ENV APISPEC_CONVERTER_VERSION=v2.11.0

RUN yarn global add "api-spec-converter@${APISPEC_CONVERTER_VERSION}" \
    && rm -rf /usr/local/share/.cache

WORKDIR /work

ENTRYPOINT ["api-spec-converter"]
CMD ["--help"]
