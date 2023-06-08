# build-docs.yml

This workflow deploys sphinx documentation and uploads it as an artifact.

## Usage

```yaml
uses: qiboteam/workflows/.github/workflows/build-docs.yml@main
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
  # poetry extra flags to add 
  # to package's installation.
  # Default: ""
  poetry-extras: ""
```
