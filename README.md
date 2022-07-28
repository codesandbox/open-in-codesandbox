# (Deprecated) Open PRs in CodeSandbox

**Note**: This action is now **deprecated**. Please install our [GitHub App](https://github.com/apps/codesandbox) for this and other great features.

---

GitHub Action that makes it easy to review your work in CodeSandbox.

![Pull request with CodeSandbox links in the description](./assets/demo-light.png#gh-light-mode-only)
![Pull request with CodeSandbox links in the description](./assets/demo.png#gh-dark-mode-only)

When you open a new pull request on your CodeSandbox project, this action will append helpful links to the end of the pull request description. With one click, you can start reviewing and testing code with a live preview environment right in your browser. Or, launch Visual Studio Code in a remote session with no hassle.

## Usage

Integrating this action into your project requires creating a GitHub Action workflow. We recommend naming the file `.github/workflows/csb.yml` — that way, we won't prompt you to install the action later on.

```yml
on: pull_request

jobs:
  open_in_codesandbox:
    name: Open in CodeSandbox
    runs-on: ubuntu-latest
    steps:
    - uses: codesandbox/open-in-codesandbox@v1
```

That's it!

By using `@v1`, you'll automatically get updates to the action as we add additional features. When it's time for us to make breaking changes with a `v2` release, nothing will suddenly break in your project.

## License

This action is licensed for use under the Apache License 2.0. For more information, please see the `LICENSE` file.
