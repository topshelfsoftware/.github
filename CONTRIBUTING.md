# Contributing

This page is dedicated to outline where to start with
questions, concerns, feature requests, or desires to contribute.

These guidelines were inspired by
[PyVista](https://github.com/pyvista/pyvista/blob/main/CONTRIBUTING.rst).

## Table of Contents

- [Reporting Issues](#reporting-issues)
- [Development Practices](#development-practices)

--------------

## Reporting Issues

Follow the practices outlined here when reporting issues
related to this repository.

### Bug Reporting

If any bugs, crashes, or concerning quirks are discovered while
using code distributed here, report it on the [issues
page](https://github.com/topshelfsoftware/.github/issues) with an appropriate
label so it can be promptly addressed. When reporting an issue, be
overly descriptive so that the behavior may be reproduced. Whenever possible,
provide tracebacks, screenshots, and sample files.

### Feature Requests

Users are encouraged to submit ideas for improvements to the code
base. Create an issue on the [issues
page](https://github.com/topshelfsoftware/.github/issues) with a
*feature-request* label to suggest an improvement. Use a descriptive
title and provide ample background information to help the developers
implement that functionality. The issue thread will be used as a place
to discuss and provide feedback.

--------------

## Development Practices

This section provides a guide to conducting development in the
repository. Follow the practices outlined here when contributing
directly to this repository.

### Branching Model

This project has a branching model that enables rapid development of
features without sacrificing stability, and closely follows the [Trunk
Based Development](https://trunkbaseddevelopment.com/) approach.

The primary features of this branching model are:

- The `main` branch is the main development branch. All features,
  patches, and other branches should be merged here. Ideally, this
  branch is functionally stable at every commit.
- There may be one or simultaneously many active branches at any given
  time. Branches should pass all applicable status checks before being merged
  into `main` as changes might introduce unintended side-effects or bugs.

### Branch Naming Conventions

To streamline development, the following are requirements for naming
branches. These requirements help the core developers know what kind of
changes any given branch is introducing before looking at the code.

- `fix/`: any bug fixes, patches, or experimental changes that are
   small (PATCH version increment expected)
- `feat/`: any changes that introduce a new feature or significant
   addition (MINOR version increment expected)
- `breaking-change/`: changes that break backward compatibility
   (MAJOR version increment expected)
- `maint/`: for general maintenance of the repository
- `doc/`: for any changes only pertaining to documentation
- `cicd/`: activity related to the CI/CD workflows
- `testing/`: improvements or changes to testing
- `release/`: changes related to a software release or tag

### Testing

Test changes locally before creating a pull request. Additionally,
add new unit tests as new functionality is added. Linting and all
unit tests will be executed after a pull request is opened.

### Creating a New Pull Request

Once a branch has been tested locally, merge into `main` by creating
a new pull request. Provide a succinct title and summarize a description
of the changes.

**ALWAYS** "Squash and Merge" when merging into `main`. This creates
a concise commit history, where the commit messages are abbreviated
summaries of the changes in each PR.
