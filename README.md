# .github

This special repository contains default [health files]((https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)) and templates for the Top Shelf Software organization.

## Contributing

See the [guidelines](./CONTRIBUTING.md) for contributing to the repositories in this organization.

## Issue Templates

Templates for creating different issues are stored in the `.github/ISSUE_TEMPLATE` directory.

## Reusable GitHub Actions Workflows

### `repo-tag-and-release.yaml`

Automatically tags a repository using the contents of a file named `VERSION` in the project root directory and subsequently
creates a release in the GitHub repository using the newly generated tag for the release.
Additionally, this workflow generates release notes that follows the same structure as GitHub's autogenerated release notes including
a `What's Changed` section with commit history and a `Full Changelog` between tag versions.

Usage:

```yaml
name: Call Tag + Release

on:
  push:
    branches:
      - main  # or any branch where you want to trigger the release workflow

jobs:
  create-release:
    uses: topshelfsoftware/.github/.github/workflows/repo-tag-and-release.yaml@main
```

> [!IMPORTANT]
> The below workflows are deprecated. Please use `repo-tag-and-release.yaml` instead.

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

### `repo-create-release.yaml`

Automatically creates a release in a repository using the contents of a file named `VERSION` in the project root directory as the tag for the release.
Additionally, this workflow generates release notes that follows the same structure as GitHub's autogenerated release notes including
a `What's Changed` section with commit history and a `Full Changelog` between tag versions.

Usage:

```yaml
name: Call Create Release

on:
  push:
    branches:
      - main  # or any branch where you want to trigger the release workflow

jobs:
  create-release:
    uses: topshelfsoftware/.github/.github/workflows/repo-create-release.yaml@main
```
