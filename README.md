# CI/CD Pipeline with GitHub Actions & Render

## 🔗 Submission Links

- 🧠 **GitHub:** [View Repository](https://github.com/PHTMGatt/20-CI-CD-GitHub-Actions)
- 🚀 **Render:** [View Live App](https://two0-ci-cd-github-actions-zubp.onrender.com)

## Overview

This project implements a CI/CD pipeline using GitHub Actions and Render. Continuous Integration runs Cypress component tests on every pull request to the `develop` branch, while Continuous Deployment automatically deploys the application to Render when code is merged into the `main` branch.

### ✅ Features

- Cypress tests run automatically on PRs to `develop`
- Deploy hook triggers deployment to Render on merge to `main`
- Two separate GitHub Actions workflows: `cypress-tests.yml` and `render-deploy.yml`
- GitFlow branching strategy: `feature/*` → `develop` → `main`

## 💻 Local Setup Instructions

```bash
# Clone the repository
git clone https://github.com/PHTMGatt/20-CI-CD-GitHub-Actions.git
cd 20-CI-CD-GitHub-Actions

# Create and push develop branch
git checkout -b develop
git push -u origin develop

# Install dependencies
npm install

# Start the app
npm start

# (Optional) Run Cypress tests manually
npx cypress open
```

## 🧪 GitHub Actions Workflows

### CI Workflow: `.github/workflows/cypress-tests.yml`

This workflow runs Cypress tests when a pull request is made to `develop`.

### CD Workflow: `.github/workflows/render-deploy.yml`

This workflow triggers a deployment to Render when code is merged to `main`.

## 🔐 GitHub Secrets Required

| Secret Name              | Purpose                              |
|--------------------------|--------------------------------------|
| `RENDER_DEPLOY_HOOK_URL` | Render deploy hook URL for deployment |

## 📝 Summary

This project demonstrates an automated approach to testing and deployment using GitHub Actions, ensuring that all changes meet quality standards before going live.
