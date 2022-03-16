# Contributing to CodeSandbox Actions

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Making Changes](#making-changes)
- [Releasing Changes](#releasing-changes)
- [Thank You](#thank-you)

## Code of Conduct

We have a code of conduct you can find [here](./CODE_OF_CONDUCT.md) and every
contributor is expected to obey the rules therein. Any issues or PRs that don't
abide by the code of conduct may be closed.

## Making Changes

Making changes to this GitHub Action requires some care, because it has the
potential to immediately impact the workflows of many repositories. Before you
continue, please think carefully about whether your proposed changes qualify
as a "breaking" change. If they do, consider how to communicate about those
changes to users.

Please also consider the following when making changes:

* Do the changes materially impact the speed of the action?
* Will the changes potentially cause the workflow to fail, potentially
  disrupting pull request processes for users?
* Do the changes introduce functionality that will be difficult to change
  in a non-breaking way?

## Releasing Changes

When this GitHub Action is implemented automatically by the CodeSandbox
platform, it tracks a major version tag (e.g. `v1`). This allows us to make
changes to the functionality (including bug fixes and minor new features)
without any intervention in the individual repositories. It also means that
we have to be careful with tag management.

When releasing a patch or minor change to the action:

1. Create a new fully-qualified tag, for example `v1.0.1`.
2. Test against this tag with an example repository as appropriate.
3. Move the major version tag, for example `v1`, to match the new version.
4. Create a Release in GitHub, including publication to the Marketplace.

When releasing a breaking change to the action:

1. Create a branch for the existing major version, for example `release-v1`.
2. Create a new fully-qualified tag, for example `v2.0.0`.
3. Test against this tag with an example repository as appropriate.
4. Create a new major version tag, for example `v2`, to match the new version.
5. Create a Release in GitHub, including publication to the Marketplace.

Further updates to previous major versions can still occur on the `release-v*`
branches, while the latest changes continue on `main`.

## Thank You

Thank you for contributing to this Action. We appreciate your time.
