# Introduction

The repository **qibogang/workflow** is a collection of reusable workflows for the Qibo Gang organization. The workflows are availaible in the folder [`github/workflows`](https://github.com/qibogang/workflows/tree/main/.github/workflows).

How to use a reusable workflow ?
================================

Suppose we want to use the **reusable workflow** `deploy-sphinx-docs-to-ghpages.yml`, all we have to do is to add the `uses` keyword in a job of our workflow, for example 

```yaml
jobs:
  call-workflow-in-local-repo:
    uses: qibogang/workflows/.github/workflows/deploy-sphinx-docs-to-ghpages.yml@main
    with:
      python-version: 3.9
```

make sure to include all the required inputs after the keyword `with`. 

For further information, see [the corresponding github page](https://docs.github.com/en/actions/using-workflows/reusing-workflows). 

Implemented workflows 
=====================

[Here](./summary.md), you can find a list of all the reusable workflows available in this repository.