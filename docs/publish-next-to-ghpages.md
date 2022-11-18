# publish-next-to-ghpages.yml

This workflow publishes Next.js website to GitHub Pages, it has no inputs.

Usage 
=====

```yaml
name: Deploy Next.js site to Pages


on: 
  workflow_dispatch:
  push:
      branches: [master]
  
jobs:

  deploy-docs:
    uses: qibogang/workflows/.github/workflows/publish-next-to-ghpages.yml@main
```