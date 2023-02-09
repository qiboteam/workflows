# deploy-pip.yml

The workflow builds the wheels and publish the repository to PyPI.

## Usage 

```yaml 

uses: qiboteam/workflow/.github/workflows/deploy-pip.yml@main
with:
    inputs:
        # The used os. 
        # Mandatory input 
        os: 'ubuntu-latest'
        # The Python version to be installed.
        # Mandatory input
        python-version: 3.9
        # If 'publish' is true the repository 
        # will be published. 
        # Default: false 
        publish: true 

secrets:
    # Token to publish 
    # Required only if 'publish' is true 
    PYPI-TOKEN: ${{secrets.PYPI_TOKEN}}
        
```
