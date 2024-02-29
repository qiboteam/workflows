# `docs.yml`

This workflow deploys sphinx documentation and uploads it as an artifact.

## Usage

```yaml
uses: qiboteam/workflows/.github/workflows/docs.yml@v2
with:
  # The python version to be installed.
  # Mandatory input
  python-version: 3.9
  # Specify the path to the dependency file
  # Mandatory input
  dependency-path: "**/poetry.lock"
  # poetry extra flags to add
  # to package's installation.
  # Default: ""
  poetry-extras: ""
```
