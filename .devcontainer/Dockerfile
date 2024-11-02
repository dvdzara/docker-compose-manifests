# kics-scan disable=965a08d7-ef86-4f14-8792-4a3b2098937e,df746b39-6564-4fed-bf85-e9c44382303c
FROM docker.io/oven/bun:1.1.34-slim@sha256:21fd0a62420d24ad6d0b2e2d82af4824d2fa24942f34f3bca539e07d149c5770

# Configure shell.
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# Configure apt.
ARG DEBIAN_FRONTEND="noninteractive"
RUN rm \
        /etc/apt/apt.conf.d/70debconf \
        /etc/apt/apt.conf.d/docker-autoremove-suggests \
        /etc/apt/apt.conf.d/docker-clean \
        /etc/apt/apt.conf.d/docker-gzip-indexes && \
    echo -e 'APT::Get::Install-Recommends "false";\nAPT::Get::Install-Suggests "false";' | tee /etc/apt/apt.conf.d/01-no-extra-pkgs

# hadolint ignore=DL3008,DL3009
RUN apt-get update && \
    apt-get install --no-install-recommends -y \
        ca-certificates \
        git \
        gpg && \
    git config --global core.editor code && \
    git config --global --add safe.directory /workspaces/docker-compose-manifests

HEALTHCHECK NONE
# hadolint ignore=DL3002
USER 0
ENTRYPOINT ["/bin/bash"]
