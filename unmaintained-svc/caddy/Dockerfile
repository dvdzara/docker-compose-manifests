FROM docker.io/library/caddy:2.8.4-builder-alpine@sha256:98bd4545236c1aae8afab0eca255903487925e92ca06f14accf7e9ca607a163e AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.8.4-alpine@sha256:fea55ae5ce2e5c07dd3d592cc34862504075d55d505d731cdc2a3f051d70d39c

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
