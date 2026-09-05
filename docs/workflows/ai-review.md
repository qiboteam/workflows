# `ai-review.yml`

The workflow runs an AI code review of a pull request with the GitHub Copilot
CLI (BYOK) and posts the findings as a pull request review: a high-level
summary plus line-specific inline comments (with optional
`suggestion` blocks). The review files and the Copilot CLI session logs are
uploaded as artifacts.

The review is triggered by a label: the caller workflow listens for the
`labeled` pull request event and calls this workflow when the PR carries the
label (default example: `run-qibot`).

## Required secrets

The caller repository must define the following secrets (BYOK provider
configuration plus a GitHub PAT for the Copilot CLI):

- `COPILOT_PROVIDER_BASE_URL`
- `COPILOT_PROVIDER_API_KEY`
- `COPILOT_PROVIDER_MAX_PROMPT_TOKENS`
- `COPILOT_PROVIDER_MAX_OUTPUT_TOKENS`
- `COPILOT_MODEL`
- `COPILOT_PAT`

## Usage

Add a caller workflow (e.g. `.github/workflows/ai-review.yml`) in the
consuming repository:

```yaml
name: ai-review

on:
  pull_request:
    types: [labeled]

jobs:
  ai-review:
    if: contains(github.event.pull_request.labels.*.name, 'run-qibot')
    uses: qiboteam/workflows/.github/workflows/ai-review.yml@main
    with:
      # Number of the pull request to review.
      # Mandatory input
      pr-number: ${{ github.event.pull_request.number }}
      # Copilot CLI BYOK provider type.
      # Default: "openai"
      provider-type: "openai"
      # Max AI credits per Copilot CLI invocation.
      # Default: 100
      max-ai-credits: 100
    secrets:
      copilot_provider_base_url: ${{ secrets.COPILOT_PROVIDER_BASE_URL }}
      copilot_provider_api_key: ${{ secrets.COPILOT_PROVIDER_API_KEY }}
      copilot_provider_max_prompt_tokens: ${{ secrets.COPILOT_PROVIDER_MAX_PROMPT_TOKENS }}
      copilot_provider_max_output_tokens: ${{ secrets.COPILOT_PROVIDER_MAX_OUTPUT_TOKENS }}
      copilot_model: ${{ secrets.COPILOT_MODEL }}
      copilot_pat: ${{ secrets.COPILOT_PAT }}
```

To run a review, add the `run-qibot` label to the pull request.
