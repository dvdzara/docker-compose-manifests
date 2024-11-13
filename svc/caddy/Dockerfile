FROM docker.io/library/caddy:2.8.4-builder-alpine@sha256:e17752ee435c363c7be26488602dfb693b256de2dbd5d21aad73b13e8f057604 AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.8.4-alpine@sha256:54e9c7289f80701f1df5bc8236b25b740f598f51f1bbdba250f2335aadd6bccd

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
