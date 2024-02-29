The repository **qiboteam/workflow** is a collection of **reusable workflows**
used by the qiboteam organization. The workflows are availaible in the folder
[`github/workflows`](https://github.com/qiboteam/workflows/tree/main/.github/workflows).

# Available workflows

- [`docs`](./docs.md)
- [`latest-stable`](./latest-stable.md)
- [`test`](./test.md)
- [`wheels`](./wheels.md)

## How to use a reusable workflow ?

If you want to use the **reusable workflow**
`deploy-sphinx-docs-to-ghpages.yml`, all you have to do is to add the `uses`
keyword in a job of your workflow, for example

```yaml
jobs:
  call-workflow-in-local-repo:
    uses: qiboteam/workflows/.github/workflows/deploy-sphinx-docs-to-ghpages.yml@main
    with:
      python-version: 3.9
      package-manager: "pip"
      dependency-path: "**/setup.py"
```
