# `docs.yml`

This workflow deploys sphinx documentation and uploads it as an artifact.

## Usage

```yaml
uses: qiboteam/workflows/.github/workflows/docs.yml@uv
with:
  # The python version to be installed.
  # Mandatory input
  python-version: "3.11"
  # uv sync extra flags to add
  # to package's installation.
  # Default: ""
  uv-extras: ""
```
