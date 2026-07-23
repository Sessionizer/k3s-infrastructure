# k3s-infrastructure

GitOps config for my k3s cluster on Hetzner CX23 (1 master, 1 worker).

ArgoCD watches this repo and applies whatever lives under `apps/`. Bootstrap stuff (ArgoCD itself, cert-manager, Traefik tweaks) was installed manually once and the manifests are kept here for reference.

## What's running

| URL | What |
|-----|------|
| https://argo.greboh.dev | ArgoCD |
| https://git.greboh.dev | Forgejo |

TLS via cert-manager + Let's Encrypt (DNS-01 through Cloudflare).
I decided to use Traefik as Ingress. This is a comfort pick, since it's what we have used at work - It also helps it ships with k3s by default

## Forgejo?
Forgejo is a self-hosted github. I wanted to do this partly for fun but also because Github is progressivley becoming unstable and slow. (But mostly for fun)
