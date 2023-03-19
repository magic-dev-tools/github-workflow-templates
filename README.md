# Github Workflow Templates

## Templates

### Publish npm package from pnpm+turborepo monorepo

```yaml
name: "[PROD] Publish"

on:
  push:
    tags:
      - "[0-9]+.[0-9]+.[0-9]+"

jobs:
  publish-readme-utils:
    uses: magic-dev-tools/github-workflow-templates/.github/workflows/template-publish-npm-package.yaml@main
    with:
      packageDir: package-dir
      packageScope: "package-scope"
    secrets:
      npm_token: ${{ secrets.NPM_TOKEN }}
```
