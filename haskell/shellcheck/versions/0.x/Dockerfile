# ShellCheck http://www.shellcheck.net

FROM alpine:3.11

ENV SHELLCHECK_VERSION=v0.7.0

RUN apk --no-cache add "bash=4.4.19-r1"
SHELL ["/bin/bash", "-o", "pipefail", "-c"]
RUN apk --no-cache --virtual=build-deps add curl \
    && tar=shellcheck-${SHELLCHECK_VERSION}.linux.x86_64.tar.xz \
    && curl -sSL https://shellcheck.storage.googleapis.com/${tar} -o shellcheck.tar.gz \
    && echo "84e06bee3c8b8c25f46906350fb32708f4b661636c04e55bd19cdd1071265112d84906055372149678d37f09a1667019488c62a0561b81fe6a6b45ad4fae4ac0  shellcheck.tar.gz" | sha512sum -c - \
    && mkdir -p /usr/src/shellcheck \
    && tar xvf shellcheck.tar.gz \
    && mv shellcheck-*/shellcheck /usr/bin/ \
    && rm -rf shellcheck* \
    && apk del --purge -r build-deps

WORKDIR /work

COPY entrypoint.sh /
RUN chmod +x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
