FROM docker.io/library/caddy:2.8.4-builder-alpine@sha256:4ac56838081008c467ae701ebf425c53db62f91e5fa723151904b9ee75d09346 AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.8.4-alpine@sha256:af32e97399febea808609119bb21544d0265c58a02836576e32a2d082c262c17

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
