FROM docker.io/library/caddy:2.8.4-builder-alpine@sha256:ce7d58e2ff641a4268d101c86db79a60d0bcdb6636a25c905c8da9a8a64b77db AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.8.4-alpine@sha256:33937b9d51461ea87794350c1c09ce53f327802508929d78f3b5642533f2f7db

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
