# deploy-sphinx-docs-to-ghpages.yml

This workflow deploys Sphinx documentation and publish it using GitHub Pages 

Usage 
=====

```yaml
name: Deploy docs


on: 
  workflow_dispatch:
  push:
      branches: [master]
  
jobs:

  deploy-docs:
    uses: qibogang/workflows/.github/workflows/deploy-sphinx-docs-to-ghpages.yml@main
    with:
      # The Python version to be installed.
      # Mandatory input value 
      python-version: 3.9
      # Documentation's path.
      # Default: ./doc 
      path-doc: ./docs
```