FROM docker.io/library/caddy:2.9.1-builder-alpine@sha256:e691e045fccb5d6d411dad22ab15860b00d6aabea521363969fa42f0aab5154b AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.9.1-alpine@sha256:eed289e78b2a0fa7d856b5d5aa9f0b39f727ab49c92f27986f1c03291c42f119

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
