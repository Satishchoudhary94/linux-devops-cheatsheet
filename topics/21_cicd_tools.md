````markdown
# ⚙️ CI/CD Tools Overview

## 🧪 Jenkins

- Open-source automation server
- Use `Jenkinsfile` to define pipelines
- Common stages: **Build → Test → Deploy**
- UI-based and script-based job management

## 🔁 GitHub Actions

- Built-in CI/CD for GitHub
- Workflow defined in `.github/workflows/main.yml`
- Trigger events: `push`, `pull_request`, `schedule`
- Integrates with any language, Docker, matrix builds

### Example:

```yaml
name: CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: echo "Build done"
```
````

🚀 GitLab CI/CD
Works with .gitlab-ci.yml file

Deep integration with GitLab repos

Uses runners to execute jobs

Auto DevOps available out of the box
