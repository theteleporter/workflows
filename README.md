# DevOps Workflows

Centralized GitHub Actions you can reuse across all your projects.

Built to automate:
- Core checks (lint, typecheck, test, build)
- Deploys (main & preview)
- Dev experience (Linear, Slack, reviewers, labels)
- Security & Insights (secret scan, bundle size, docs)

---

## ⚙️ Core Dev Workflows

| Workflow File           | Description                             |
|------------------------|-----------------------------------------|
| `lint.yml`             | Runs ESLint + Prettier checks           |
| `typecheck.yml`        | Runs `tsc --noEmit`                     |
| `unit-tests.yml`       | Runs test suite (Jest, Vitest)          |
| `build-check.yml`      | Ensures Next.js / Vite app builds       |

---

## 🚀 Deployment

| Workflow File                | Description                           |
|-----------------------------|---------------------------------------|
| `deploy-vercel-main.yml`    | Auto-deploy to Vercel on main push    |
| `deploy-vercel-preview.yml` | Preview deploys on PR + Slack notify  |

---

## 💬 Team/Productivity

| Workflow File       | Description                              |
|---------------------|------------------------------------------|
| `linear-link.yml`   | Auto-link PRs to Linear + close tasks    |
| `pr-labeler.yml`    | Add PR labels based on file patterns     |
| `assign-reviewers.yml` | Auto-assign code reviewers            |

> Note: includes `.github/labeler.yml` and `auto_assign.yml` configs

---

## ⚡ Advanced / Extras

| Workflow File        | Description                             |
|----------------------|-----------------------------------------|
| `docker-build.yml`   | Build & push Docker image to GHCR       |
| `bundle-size.yml`    | Comments bundle size on PRs             |
| `secrets-scan.yml`   | Blocks secret leaks using Gitleaks      |
| `generate-docs.yml`  | Builds + commits docs on tag push       |
| `cron-cleanup.yml`   | Example CRON job (e.g., clean temp)     |

---

## 🚀 Usage in Another Repo

You can:
1. Copy & paste from here
2. Or (soon): use reusable workflows like this:

```yaml
uses: theteleporter/workflows/.github/workflows/lint.yml@main

```

---
## 🧪 Coming Soon

- Cypress / Playwright e2e workflows

- SonarQube or Codecov

- Sentry integration

---

By [@theteleporter](https://github.com/theteleporter)
