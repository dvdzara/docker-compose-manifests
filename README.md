# Infrastructure as code manifests

These files describe the things that I deploy on my homelab.

## Tools needed for kubernetes

- age (generate key for sops): [https://github.com/FiloSottile/age]
- helm
- kubectl
- kustomize
- sops (secret encryption): [https://github.com/getsops/sop]

## Secrets

Secrets are encrypted using sops. If you want to use them you will have to
generate a secret key and generate new ones.
