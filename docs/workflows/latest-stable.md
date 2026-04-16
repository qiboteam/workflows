# `latest-stable.yml`

This workflow deploys the `latest` and `stable` sphinx documentations and publish them using github pages.

## Usage

```yaml
uses: qiboteam/workflows/.github/workflows/latest-stable.yml@uv
with:
  # The python version to be installed.
  # Mandatory input
  python-version: "3.11"
  # Project's name
  # Mandatory input
  project: qibo
  # Url where to pubish the documentation
  # Default: https://qibo.science/
  url: https://this/is/an/example
  # Label classifing the trigger (e.g. 'latest' or 'stable')
  # Default: none
  trigger-label: latest
  # uv sync extra flags to add
  # to package's installation.
  # Default: ""
  uv-extras: ""
```
