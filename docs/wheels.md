# `wheels.yml`

The workflow builds the wheels and publish the repository to PyPI.

## Usage

```yaml
uses: qiboteam/workflow/.github/workflows/wheels.yml@main
with:
  inputs:
    # The used os.
    # Mandatory input
    os: "ubuntu-latest"
    # The python version to be installed.
    # Mandatory input
    python-version: 3.9
    # If 'publish' is true the repository
    # will be published.
    # Default: false
    publish: true
    # poetry extra flags to add
    # to package's installation.
    # Default: ""
    poetry-extras: ""

secrets:
  # Token to publish
  # Required only if 'publish' is true
  PYPI-TOKEN: ${{secrets.PYPI_TOKEN}}
```
