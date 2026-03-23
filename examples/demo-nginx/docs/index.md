# Demo CNCF NBG

Welcome to the TechDocs documentation-as-code sample for the `demo-nginx-cncf-nbg` component.

This documentation is built automatically by TechDocs from this repository content.

- Component: `demo-nginx-cncf-nbg`
- Type: service
- Lifecycle: experimental

## Overview

This is a minimal nginx deployment used in the Backstage demo workload sample.

## CI/CD workflow

Use `examples/template/template.yaml` (Demo NGINX CI/CD Template) as your starting point.

- scaffolder creates component in GitHub
- `.github/workflows/ci.yaml` runs CI
- TechDocs from `docs/` path is built via `mkdocs.yml`
- component in Backstage `CI/CD` tab (or `EntityPage` if plugin enabled) can show GitHub Actions status.

