# Documentation 

It follows a list of all the implemented workflows:

- [`publish-next-to-ghpages`](./publish-next-to-ghpages.md):

    publish Next.js website to GitHub Pages, this workflow has no inputs.

- [`deploy-sphinx-docs-to-ghpages`](../.github/workflows/deploy-sphinx-docs-to-ghpages.yml):

    deploy Sphinx documentation and publish it using GitHub Pages 
    
    **Inputs:** 

    * **python-version** (*string*): (Mandatory) the Python version to be installed 
    * **path-doc** (*string*): (Optional) documentation's path. The default value is `./doc`. 