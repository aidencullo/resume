# Resume Repo Setup

## Branches
- `dev` - working branch for edits
- `prod` - production branch, merged manually via PR from dev

## Branch Protection (prod)
- Requires PR (no direct pushes)
- 1 required approving review (no CLI or self-merge)
- No force pushes

## Workflow
1. Edit on `dev` branch
2. Push changes to `dev` — triggers a build of both dev and prod PDFs, deploys both to GitHub Pages
3. Preview changes at https://aidencullo.github.io/resume/dev/resume.pdf
4. When ready, create a PR from `dev` → `prod` and merge via GitHub UI
5. Merging to `prod` triggers another deploy, updating the prod PDF

## GitHub Pages URLs
- prod: https://aidencullo.github.io/resume/resume.pdf
- dev: https://aidencullo.github.io/resume/dev/resume.pdf

## Deployment (`.github/workflows/deploy-pages.yml`)
Every push to `dev` or `prod` triggers the workflow, which:
1. Builds a PDF from the `prod` branch
2. Builds a PDF from the `dev` branch
3. Deploys both together — prod PDF at root, dev PDF at `/dev/`

This avoids the overwrite problem where a dev push would wipe the prod deployment.
