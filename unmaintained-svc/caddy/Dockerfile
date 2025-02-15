FROM docker.io/library/caddy:2.9.1-builder-alpine@sha256:5875c0886d07aeae49c25c284bb5c7b65c2506f16e783cdb1f6f981200f3a226 AS builder

RUN xcaddy build --with github.com/caddy-dns/cloudflare

FROM docker.io/library/caddy:2.9.1-alpine@sha256:b60636634fd2aebaf9460cf60997ad83aad6b139318d5713e2b78a60f52b139c

COPY --from=builder /usr/bin/caddy /usr/bin/caddy

USER 41380:41380
HEALTHCHECK NONE
