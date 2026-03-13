# Resume Repo Setup

## Branches
- `dev` - working branch for edits
- `prod` - production branch, deployed to GitHub Pages

## Branch Protection (prod)
- Requires 1 approving review
- No force pushes
- No direct pushes - must use PR
- Admin enforcement enabled

**IMPORTANT:** Once admin enforcement is enabled, even repo admins cannot bypass. To make rules unchangeable, transfer repo to an organization.

## Workflow
1. Edit on `dev` branch
2. Push changes to `dev` - auto-deploys to https://aidencullo.github.io/resume/resume-dev.pdf
3. Create PR from `dev` → `prod`
4. Review and merge PR - auto-deploys to https://aidencullo.github.io/resume/resume.pdf

## GitHub Pages URLs
- dev: https://aidencullo.github.io/resume/resume-dev.pdf
- prod: https://aidencullo.github.io/resume/resume.pdf

## Local Pre-push Hook
Located at `.git/hooks/pre-push` - blocks pushing directly to prod locally.
