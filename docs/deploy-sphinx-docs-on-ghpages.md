# deploy-sphinx-docs-on-ghpages.yml

This workflow deploys sphinx documentation and publishes it using github pages.

## Usage

```yaml
uses: qiboteam/workflows/.github/workflows/deploy-sphinx-docs-on-ghpages.yml@main
with:
  # The python version to be installed.
  # Mandatory input
  python-version: 3.9
  # Specify the path to the dependency file
  # Mandatory input
  dependency-path: '**/pyproject.toml'
  # Documentation's path.
  # Default: ./doc
  path-doc: ./docs
```
