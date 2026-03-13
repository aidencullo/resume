# Resume Repo Setup

## Branches
- `dev` - working branch for edits
- `prod` - production branch, deployed to GitHub Pages

## Branch Protection (prod)
- Requires 1 approving review
- No force pushes
- No direct pushes - must use PR
- Admin enforcement enabled

## Workflow
1. Edit on `dev` branch
2. Push changes to `dev`
3. Create PR from `dev` → `prod`
4. Review and merge PR
5. Manually trigger deploy workflow or auto-deploys on merge

## GitHub Pages
- URL: https://aidencullo.github.io/resume/
- PDF: https://aidencullo.github.io/resume/resume.pdf
- Source: `prod` branch

## Local Pre-push Hook
Located at `.git/hooks/pre-push` - blocks pushing directly to prod locally.
