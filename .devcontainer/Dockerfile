FROM docker.io/library/alpine:3.20.3

# hadolint ignore=DL3018
RUN apk add --no-cache git gpg && \
    git config --global core.editor code && \
    git config --global --add safe.directory /workspace/unitn-ice-notes

# hadolint ignore=DL3002
USER 0:0
ENTRYPOINT []
HEALTHCHECK NONE
