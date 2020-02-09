FROM python:3.8.1-alpine3.11

ENV YQ_VERSION=2.10.0

RUN apk --no-cache add jq bash \
    && pip3 install "yq==${YQ_VERSION}" \
    && find / -depth -type d -name __pycache__ -exec rm -rf {} \; \
    && rm -rf /root/.cache /lib/apk/db \
    && mkdir -p /lib/apk/db

WORKDIR /work

CMD ["yq", "--help"]
