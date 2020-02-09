FROM node:12.15.0-alpine3.11

ENV NEWMAN_VERSION=4.5.7

RUN yarn global add "newman@${NEWMAN_VERSION}" \
    && rm -rf /usr/local/share/.cache

WORKDIR /work

ENTRYPOINT ["newman"]
CMD ["run", "--help"]
