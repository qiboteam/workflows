The repository **qiboteam/workflow** is a collection of **reusable workflows** used
across the qiboteam organization. The workflows are availaible in the folder
[`github/workflows`](https://github.com/qiboteam/workflows/tree/v2/.github/workflows).

# Available workflows

- [`ai-review`](./workflows/ai-review.md)
- [`test`](./workflows/test.md)
- [`wheels`](./workflows/wheels.md)
- [`docs`](./workflows/docs.md)
- [`latest-stable`](./workflows/latest-stable.md)
- [`selfhosted`](./workflows/selfhosted.md)

## How to run a reusable workflow ?

Using `docs.yml` as an example, the only action required is to add the `uses` keyword in
a job of the caller workflow, e.g.

```yaml
jobs:
  caller-job:
    uses: qiboteam/workflows/.github/workflows/docs.yml@main
    with:
      python-version: "3.11"
```

# Actions

For workflows developers: some workflows' building blocks are split as individual
[actions](./actions).
