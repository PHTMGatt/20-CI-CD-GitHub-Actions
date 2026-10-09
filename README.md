# CI/CD Pipeline with GitHub Actions & Render

## Submission Links

- **GitHub:** [View Repository](https://github.com/PHTMGatt/20-CI-CD-GitHub-Actions)
- **Render:** [View Live App](https://two0-ci-cd-github-actions-zubp.onrender.com)

## Overview

This project demonstrates a CI/CD workflow using GitHub Actions, Cypress component tests, and Render deployment automation.

Continuous Integration runs Cypress component tests for pull requests targeting `develop` or `main`. Continuous Deployment validates and builds merged pull requests to `main`, then triggers the existing Render deploy hook once.

## Features

- Cypress component tests on pull requests to `develop` and `main`
- Production build verification before deployment
- Render deployment only after a pull request is actually merged into `main`
- Separate CI and CD workflows
- GitFlow-friendly branching: `feature/*` → `develop` → `main`

## Local Setup

```bash
git clone https://github.com/PHTMGatt/20-CI-CD-GitHub-Actions.git
cd 20-CI-CD-GitHub-Actions
npm install
npm start
```

Run the Cypress component tests with:

```bash
npm run test-component
```

## GitHub Actions Workflows

### CI: `.github/workflows/tests.yml`

Runs the application build and Cypress component tests for pull requests targeting `develop` or `main`.

### CD: `.github/workflows/deploy.yml`

Runs only when a pull request into `main` is closed **and merged**. The workflow installs dependencies, verifies the production build, then triggers the Render deploy hook once.

## GitHub Secret Required

| Secret | Purpose |
| --- | --- |
| `RENDER_DEPLOY_HOOK` | Render deploy hook URL used by the CD workflow |

## Summary

The project demonstrates automated quality checks before merge and controlled deployment to Render after successful merges to the production branch.
