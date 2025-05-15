# CI/CD Pipeline with GitHub Actions & Render

## 🔗 Live Links

- 🔍 **GitHub Repository:** [PHTMGatt/20-CI-CD-GitHub-Actions](https://github.com/PHTMGatt/20-CI-CD-GitHub-Actions)
- 🌐 **Deployed Application:** [two0-ci-cd-github-actions-zubp.onrender.com](https://two0-ci-cd-github-actions-zubp.onrender.com)


## Overview

This project implements a CI/CD pipeline using GitHub Actions and Render. Continuous Integration runs Cypress component tests on every pull request to the `develop` branch, while Continuous Deployment automatically deploys the application to Render when code is merged into the `main` branch.

### ✅ Features

- Cypress tests run automatically on PRs to `develop`
- Deploy hook triggers deployment to Render on merge to `main`
- Two separate GitHub Actions workflows: `cypress-tests.yml` and `render-deploy.yml`
- GitFlow branching strategy: `feature/*` → `develop` → `main`

```bash
# Clone the repository
git clone https://github.com/your-username/your-repo.git
cd your-repo

# Create and push develop branch
git checkout -b develop
git push -u origin develop

# Install dependencies
npm install

# Start the app
npm start

# (Optional) Run Cypress tests manually
npx cypress open
