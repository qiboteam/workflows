# rules-poetry.yml

The workflow runs the tests and the documentation examples of the packages managed by `poetry`. 
It also can evaluate the coverage and update `Codecov`.

If `Dependabot` is present in the repo and the `codecov_token` is used, this could generate [issues](https://github.com/qiboteam/qibocal/pull/238), since `Dependabot` has no access to the repo secrets. 

For public repos, the `codecov_token` is not [required](https://docs.codecov.com/docs/frequently-asked-questions/#where-is-the-repository-upload-token-found), otherwise see [here](https://docs.github.com/en/code-security/dependabot/working-with-dependabot/configuring-access-to-private-registries-for-dependabot
) to enable the access.

## Usage 

```yaml 

uses: qiboteam/workflow/.github/workflows/rules-poetry.yml@main
with:
    inputs:
        # The used os. 
        # Mandatory input 
        os: 'ubuntu-latest'
        # The Python version to be installed.
        # Mandatory input
        python-version: 3.9
        # Poetry extra flags to add 
        # to package's installation.
        # Default: ""
        poetry-extras: ""
        # If 'doctest' is true the documentation 
        # examples will be tested.
        # Default: false
        doctests: true 
            
secrets:
    # Token to update Codecov.
    codecov_token: ${{ secrets.codecov_token }}
        
```
