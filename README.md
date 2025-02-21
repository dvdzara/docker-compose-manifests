# Infrastructure as code manifests

These files describe the things that I deploy on my homelab.

## Tools needed for kubernetes

- kubectl
- sops (secret encryption): [https://github.com/getsops/sop]
- age (generate key for sops): [https://github.com/FiloSottile/age]

## Secrets

Secrets are encrypted using sops. If you want to use them you will have to
generate a secret key and generate new ones.
