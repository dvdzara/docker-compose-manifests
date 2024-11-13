FROM docker.io/library/caddy:2.8.4-builder-alpine@sha256:90cd820a7dbd48d507151f66cbece01af0f90d10fed172dbcfa6ce631f42967c AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.8.4-alpine@sha256:5d4e02f275d12136a8e0a487e765ce459a00d49e23b543e9cd8190562ec5d27b

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
