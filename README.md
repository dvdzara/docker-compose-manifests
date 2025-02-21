# Docker compose manifests

I use these manifests to deploy services on my server.

## Tools needed for kubernetes

- kubectl
- sops (secret encryption): [https://github.com/getsops/sop]
- age (generate key for sops): [https://github.com/FiloSottile/age]

## Secrets

Secrets are encrypted using sops. If you want to use them you will have to
generate a secret key and generate new ones.
