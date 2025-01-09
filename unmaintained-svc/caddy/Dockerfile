FROM docker.io/library/caddy:2.9.1-builder-alpine@sha256:d1f4052b4200e92895c9733cade27a82dbb27f358c51a5ef6428206d390b2d6a AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.9.1-alpine@sha256:e70ccf0c9821a88303671ef22d7b5e2d2b6057a8b18703022d755ba4d5fd35cd

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
