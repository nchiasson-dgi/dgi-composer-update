# Update Composer packages

Workflow for updating packages of a particular namespace and issuing a pull request.

## Usage

### Inputs

- `github-token`: GitHub access token.

### Example Workflow

```yaml
---
name: Update composer project
on:
  schedule:
    - cron: '0 0 * * SUN'
  workflow_dispatch:

jobs:
  update:
    uses: discoverygarden/dgi-composer-update:v1
    secrets: inherit
    with:
      github-token: ${{ secrets.GITHUB_TOKEN }}
```
