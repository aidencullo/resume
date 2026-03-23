# Resume

LaTeX resume built and deployed via GitHub Actions.

## Branches

- `dev` — active development
- `staging` — pre-production review
- `prod` — production (default branch)

Flow: `dev` → `staging` → `prod`

### After merging, reset source branch to target

- Merge `staging` → `prod`, then reset `staging` to `prod`
- Merge `dev` → `staging`, then reset `dev` to `staging`

This keeps all branches in sync after promotion.

## Deployments

- **Prod:** https://aidencullo.github.io/resume/resume.pdf
- **Staging:** https://aidencullo.github.io/resume/staging/resume.pdf
- **Dev:** https://aidencullo.github.io/resume/dev/resume.pdf

## Workflows

- `deploy-pages.yml` — builds dev, staging, and prod LaTeX → PDF, deploys to GitHub Pages
- `enforce-branch.yml` — enforces branch promotion order (dev → staging → prod)
