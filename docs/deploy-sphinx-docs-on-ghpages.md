# deploy-sphinx-docs-on-ghpages.yml

This workflow deploys sphinx documentation and publishes it using github pages.

## Usage

```yaml
uses: qiboteam/workflows/.github/workflows/deploy-sphinx-docs-on-ghpages.yml@main
with:
  # The python version to be installed.
  # Mandatory input
  python-version: 3.9
  # Choose one package manager between 'pip' and 'poetry'
  # Mandatory input
  package-manager: 'pip'
  # Specify the path to the dependency file
  # Mandatory input
  dependency-path: '**/setup.py'
  # Documentation's path.
  # Default: ./doc
  path-doc: ./docs
```
