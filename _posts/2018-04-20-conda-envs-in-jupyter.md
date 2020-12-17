---
layout: post
title: Using conda environments in Jupyter Lab notebooks
image: 
tags: conda Jupyter
---

There are some great tips from Peter Bull at Driven Data about the proper way to set up data science projects [here](https://github.com/drivendata/data-science-is-software) and [here](https://github.com/drivendata/cookiecutter-data-science).

One of the suggestions is to create a new environment for each project, so that you can create a list of the packages with the working versions to include as a `requirements.txt` file (or in the case of conda, an `environment.yml` file). But I use Jupyter, and I couldn't figure out how to get the environments to show up in the list of kernels.

The three part solution is:

1. Install [`nb_conda_kernels`](https://github.com/Anaconda-Platform/nb_conda_kernels).
2. Create and activate the project's environment (`conda create --name MY-ENV pandas; source activate MY-ENV`).
3. In the project's environment, `conda install ipykernel` so that it is available from within Jupyter/iPython.

Now you can have easy access to a specific environment for each project.
