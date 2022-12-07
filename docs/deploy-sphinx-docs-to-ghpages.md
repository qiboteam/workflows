# deploy-sphinx-docs-to-ghpages.yml

This workflow deploys Sphinx documentation and publishes it using GitHub Pages.

## Usage

```yaml
uses: qibogang/workflows/.github/workflows/deploy-sphinx-docs-to-ghpages.yml@main
with:
  # The Python version to be installed.
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
