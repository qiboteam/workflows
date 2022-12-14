# deploy-ghpages-latest-stable.yml

This workflow deploys the `latest` and `stable` Sphinx documentations and publish them using GitHub Pages.

## Usage

```yaml
uses: qibogang/workflows/.github/workflows/deploy-ghpages-latest-stable.yml@main
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
  # Project's name 
  # Mandatory input 
  project: qibo
  # Url where to pubish the documentation
  # Default: https://qibo.science/
  url: https://this/is/an/example
  # label classifing the trigger (e.g. 'latest' or 'stable')
  # Default: none 
  trigger-label: latest 
  # Documentation's path.
  # Default: ./doc
  path-doc: ./docs
```
