# Setup

1. Ensure the `demo-nginx-cncf-nbg` component is registered in `examples/entities.yaml`.
2. `backstage.io/techdocs-ref: dir: demo-nginx` is used to point TechDocs to this folder.
3. Run Backstage app and verify TechDocs page appears for `demo-nginx-cncf-nbg` via catalog.

## Full demo workflow (scaffold -> GH -> Backstage)

1. In Backstage, open **Software templates** and choose **Demo NGINX CI/CD Template**.
2. Fill in Component name (e.g. `demo-nginx-cncf-nbg`) and GitHub repository URL (e.g. `https://github.com/<your-account>/demo-nginx-cncf-nbg`).
3. Execute scaffolder. It creates the repository, commits all template content, and registers the component in the catalog.
4. In GitHub:
   - Verify `.github/workflows/ci.yaml` exists
   - Verify `docs/` and `mkdocs.yml` exist
   - Verify `catalog-info.yaml` has annotations for TechDocs and the optional GitHub Actions project slug
5. Backstage:
   - Find the component in Catalog, open it
   - `Data` card should show component metadata
   - `Docs` tab should show generated TechDocs content from `docs/index.md`
   - `CI/CD` tab (as configured in `packages/app/src/components/catalog/EntityPage.tsx`) can show CI status if a CI plugin like `@backstage-community/plugin-github-actions` is installed and configured

## Quick path to update existing demo-nginx entity

For your existing `demo-nginx-cncf-nbg` entity, add:

```yaml
metadata:
  annotations:
    github.com/project-slug: "<your-org>/<your-repo>"
    backstage.io/techdocs-ref: "dir: demo-nginx"
```

Then validate in Backstage Catalog and TechDocs.
