# Analyze

Runs the `poe lint` and `poe lint-warnings` tasks. Set `types` to `true` to
also run a project's optional `poe types` task.

## Usage

```yaml
- uses: qiboteam/workflows/actions/uv/analyze@uv_pytest
  with:
    types: true
```
