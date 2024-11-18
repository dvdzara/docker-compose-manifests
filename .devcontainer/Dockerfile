# kics-scan disable=d3499f6d-1651-41bb-a9a7-de925fea487b

FROM docker.io/library/alpine:3.20.3@sha256:1e42bbe2508154c9126d48c2b8a75420c3544343bf86fd041fb7527e017a4b4a

# hadolint ignore=DL3018
RUN apk add --no-cache git gpg && \
    git config --global core.editor code && \
    git config --global --add safe.directory /workspace/docker-compose-manifests

# hadolint ignore=DL3002
USER 0:0
ENTRYPOINT []
HEALTHCHECK NONE
