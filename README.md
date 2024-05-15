# Website for Cefas and Aries Python course 2024

https://ueapy.github.io/pythoncourse2024-website/


Steps to generate pages using mkdocs:
1. Create and activate conda environment using environment.yaml

    1st time
    conda env create

    then
    conda activate mkdocs

2. Generate pages from markdown files and deploy to github as a branch gh-pages

    mkdocs gh-deploy --clean
