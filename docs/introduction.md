# Introduction

The repository **qibogang/workflow** is a collection of reusable workflows for the Qibo Gang organization. The workflows are availaible in the folder [`github/workflows`](./.github/workflows/).

# How to use a reusable workflow ?

Suppose we want to use the **reusable workflow** `deploy-sphinx-docs-to-ghpages.yml`, all we have to do is to add the `uses` keyword in a job of our workflow, for example 

```yaml
jobs:
  call-workflow-in-local-repo:
    uses: qibogang/workflows/.github/workflows/deploy-sphinx-docs-to-ghpages.yml@main
    with:
      python-version: 3.9
```

make sure to include all the required inputs with the keyword `with`. 

For further information, see [the corresponding github page](https://docs.github.com/en/actions/using-workflows/reusing-workflows). 

# Documentation 

It follows a list of all the implemented workflows:

- [`publish-next-to-ghpages`](./.github/workflows/publish-next-on-ghpages.yml):

    publish Next.js website to GitHub Pages, this workflow has no inputs.

- [`deploy-sphinx-docs-to-ghpages`](./.github/workflows/deploy-sphinx-docs-to-ghpages.yml):

    deploy Sphinx documentation and publish it using GitHub Pages 
    
    **Inputs:** 

    * **python-version** (*string*): (Mandatory) which Python version has to be installed
    * **path-doc** (*string*): (Optional) documentation's path. The default value is `./doc`. 