FROM docker.io/library/caddy:2.8.4-builder-alpine@sha256:edc6e5121f18919c8f0acb4c578a271ce1806d1a5f0bfd15180b17eedcccd793 AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.8.4-alpine@sha256:886f7caa715bd1d31c8a0253841a441d93d5fe374b9d9a3e3cf675088d3ab9ce

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
