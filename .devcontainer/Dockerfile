FROM docker.io/library/alpine:3.21.3@sha256:a8560b36e8b8210634f77d9f7f9efd7ffa463e380b75e2e74aff4511df3ef88c

# hadolint ignore=DL3018
RUN apk add --no-cache git gpg kubectl kustomize sops age helm

COPY --from=docker.io/fluxcd/flux-cli:v2.5.0@sha256:3c9606b188aeef772e5a1ce05debf49d5f8674ec20ab5eab14ab06b07b6d5d4e /usr/local/bin/flux /usr/local/bin/

# hadolint ignore=DL3002
USER 0:0
ENTRYPOINT []
HEALTHCHECK NONE
