FROM docker.io/library/caddy:2.9.1-builder-alpine@sha256:d1f4052b4200e92895c9733cade27a82dbb27f358c51a5ef6428206d390b2d6a AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.9.1-alpine@sha256:7773b17cbe3a5a6c08131d23424b159df435ad7f457ba9f95b627eb245f46403

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
