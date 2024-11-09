# .github

This special repository contains default [health files]((https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)) and templates for the Top Shelf Software organization.

## Contributing

See the [guidelines](./CONTRIBUTING.md) for contributing to the repositories in this organization.

## Issue Templates

Templates for creating different issues are stored in the `.github/ISSUE_TEMPLATE` directory.

## Reusable GitHub Actions Workflows

### `repo-auto-tag.yaml`

Automatically tags a repository using the contents of a file named `VERSION` in the project root directory.

Usage:

```yaml
name: Tag Repository Call

on:
  push:
    branches:
      - main  # or any branch where you want to trigger the release workflow

jobs:
  tag-repo:
    uses: topshelfsoftware/.github/.github/workflows/repo-auto-tag.yaml@main
```
