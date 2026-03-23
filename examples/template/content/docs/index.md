# ${{ values.name }}

This component is scaffolded using `demo-nginx-cncf-nbg-cicd-template`.

- service: NGINX placeholder
- docs: TechDocs is served from this repository (`docs/`)
- CI: GitHub Actions at `.github/workflows/ci.yaml`
- creator: `${{ values.creatorDisplayName }}`
- owner: `${{ values.owner }}`

## What this provides

1. Backstage catalog component with TechDocs annotation
2. GitHub Actions pipeline including lint + docs verify
3. CI/CD tab can show checks via integration plugin
