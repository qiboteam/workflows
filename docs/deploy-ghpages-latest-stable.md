# deploy-ghpages-latest-stable.yml

This workflow deploys the `latest` and `stable` sphinx documentations and publish them using github pages.

## Usage

```yaml
uses: qiboteam/workflows/.github/workflows/deploy-ghpages-latest-stable.yml@main
with:
  # The python version to be installed.
  # Mandatory input
  python-version: 3.9
  # Specify the path to the dependency file
  # Mandatory input
  dependency-path: '**/pyproject.toml'
  # Project's name
  # Mandatory input
  project: qibo
  # Url where to pubish the documentation
  # Default: https://qibo.science/
  url: https://this/is/an/example
  # Label classifing the trigger (e.g. 'latest' or 'stable')
  # Default: none
  trigger-label: latest
  # Documentation's path.
  # Default: ./doc
  path-doc: ./docs
  # poetry extra flags to add 
  # to package's installation.
  # Default: ""
  poetry-extras: ""
```
