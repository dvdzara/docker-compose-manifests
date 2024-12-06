# kics-scan disable=d3499f6d-1651-41bb-a9a7-de925fea487b

FROM docker.io/library/alpine:3.21.0@sha256:21dc6063fd678b478f57c0e13f47560d0ea4eeba26dfc947b2a4f81f686b9f45

# hadolint ignore=DL3018
RUN apk add --no-cache git gpg && \
    git config --global core.editor code && \
    git config --global --add safe.directory /workspace/docker-compose-manifests

# hadolint ignore=DL3002
USER 0:0
ENTRYPOINT []
HEALTHCHECK NONE
