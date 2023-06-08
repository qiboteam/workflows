# selfhosted.yml

...

## Usage 

```yaml 

uses: qiboteam/workflow/.github/workflows/selfhosted.yml@main
with:
    inputs:
        used-labels: 
        python-version: 3.9
        artifact-url:
        poetry-extras:


secrets:
    repo_token: ${{ secrets.GITHUB_TOKEN }}
        
```
