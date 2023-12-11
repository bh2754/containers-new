FROM ghcr.io/bh2754/alpine:rolling@sha256:81a3862c3a27e8ebc9a67f78f20ce36af2bdc25087d9195ee7c1379e0318c0b8

ARG TARGETPLATFORM
ARG VERSION
ARG CHANNEL

#hadolint ignore=DL3018
RUN apk add --no-cache ca-certificates postgresql16-client~"${VERSION}"

USER kah

COPY ./apps/postgres-init/entrypoint.sh /entrypoint.sh

CMD ["/entrypoint.sh"]

LABEL org.opencontainers.image.source="https://github.com/postgres/postgres"
