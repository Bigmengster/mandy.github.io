# Mandy

This repo contains the source code to build this [Github-page](https://yhuang85.github.io/mandy/) where I write about stuff that I find interesting.

## Build tools
The Github page is served from the **docs** folder, which is automatically generated by [Sphinx](https://www.sphinx-doc.org) - a software primarily designed for documenting Python projects and clearly abused here. Details about the build can be found in the official [Sphinx tutorial](https://www.sphinx-doc.org/en/master/tutorial/index.html). In particular, I heavily use [MathJax 3](https://www.mathjax.org/) supported by Sphinx 4 for rendering math. My MathJax configurations can be found in **build-source/source/conf.py**, which actually hosts all Sphinx configurations. On top of Sphinx, I've made the following personal choices:

- [Pipenv](https://pipenv.pypa.io/en/latest/) is used to manage Python packages.

- [Pydata-Sphinx-Theme](https://github.com/pydata/pydata-sphinx-theme) is used to style the website.

- [Inkscape](https://inkscape.org) is used to draw pictures in the format of SVG files.

- Since Github page can only be rendered under certain path (I use **main/docs**), I followed suggestions in this [post](https://www.docslikecode.com/articles/github-pages-python-sphinx/) to organize folders in this repo.

## Work with the repo
- Run `pipenv run make livehtml` within the folder **build-source** to view the changes live on `localhost:8000`.

- Run `pipenv run make github` within the folder **build-source** to create the source files for the GitHub-page and copy them to the **docs** folder.
