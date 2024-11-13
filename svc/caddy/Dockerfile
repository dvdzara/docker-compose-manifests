FROM docker.io/library/caddy:2.8.4-builder-alpine@sha256:90cd820a7dbd48d507151f66cbece01af0f90d10fed172dbcfa6ce631f42967c AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.8.4-alpine@sha256:e97e0e3f8f51be708a9d5fadbbd75e3398c22fc0eecd4b26d48561e3f7daa9eb

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
