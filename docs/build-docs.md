# build-docs.yml

This workflow deploys Sphinx documentation and uploads it as an artifact.

## Usage

```yaml
uses: qibogang/workflows/.github/workflows/build-docs.yml@main
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
