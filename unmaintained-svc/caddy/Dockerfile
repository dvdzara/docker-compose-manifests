FROM docker.io/library/caddy:2.9.1-builder-alpine@sha256:bfa436d2711d1294501ba0f72f149d8c5dad237fc8e9c9b9aec682df8438ec73 AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.9.1-alpine@sha256:7773b17cbe3a5a6c08131d23424b159df435ad7f457ba9f95b627eb245f46403

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
