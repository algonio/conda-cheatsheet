# conda-cheatsheet
Quick overview of most useful conda commands

## Show existing environments
* `conda env list`
* `conda info --envs`

## Create new environment
* `conda create -n py39 python=3.9`
  * Env with pure Python
* `conda create -n py39 python=3.9 -c conda-forge`
  * Env with pure Python from conda-forge
* `conda create -n py39 anaconda python=3.9`
  * Build environment with all Anaconda packages

## Install packages
* `conda install pandas`
* `conda install pandas==0.25`
  * Install specific version of library
* `conda install -c conda-forge pandas`
  * Install from conda-forge repository

## Update packages
* `conda update pandas`
* `conda update pandas --no-deps`
  * Update without updating all dependencies
* `conda update --all`
  * Update all packages in env

## Remove environment
* `conda remove -n py39 --all`

## Export environment
* `conda env export  --no-builds > environment.yaml`

## Recreate env from export
* `conda env create -f environment.yaml`
