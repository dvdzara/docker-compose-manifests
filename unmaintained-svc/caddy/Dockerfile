FROM docker.io/library/caddy:2.9.1-builder-alpine@sha256:77a6376a7f8074e856ffdb339054d28b93bd6cc68c82e34b675b0b39b1a25689 AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.9.1-alpine@sha256:89ea4dae338296f09e236f619460928e6431376a0bc4e1e4017f7ad057ef2b18

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
