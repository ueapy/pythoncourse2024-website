# Website for Cefas and Aries Python course 2024

https://ueapy.github.io/pythoncourse2024-website/


Steps to generate pages using mkdocs:

1. Check that the repo Settings > Pages

* Build and deployment
  * Branch > gh-pages and /root

2. Create and activate conda environment using environment.yaml

    1st time
    conda env create

    then
    conda activate mkdocs

3. Generate pages from markdown files and deploy to github as a branch gh-pages

    ```
    mkdocs gh-deploy --clean
    ```

    To generate pages into the _site directory, without pushing to github

    ```
    mkdocs build
    ```



