##### Jonathan Sedar Personal Project

# PyMC3 Vs PyStan Comparison
_Spring 2016_


This set of Notebooks and scripts comprise the **pymc3_vs_pystan** personal project by Jonathan Sedar of Applied AI Ltd, written primarily for presentation at the PyData London 2016 Conference.

The project demonstrates hierarchical linear regression using two Bayesian inference frameworks: PyMC3 and PyStan. The project borrows heavily from code written for Applied AI Ltd and is supplied here for educational purposes only. No copyright or license is extended to users.

Copyright Applied AI Ltd 2016


---


# Development

## Git clone the repo to your workspace.

e.g. in Mac OSX terminal:

        $> git clone https://github.com/jonsedar/pymc3_vs_pystan.git
        $> cd pymc3_vs_pystan



## Setup a virtual environment for Python libraries

**NOTE:** using Python 3.5

Using Anaconda distro,

1. create a new virtual env, installing packages from env YAML file:


        $> conda env create --file conda_env_pymc3_vs_pystan.yml
        $> source activate pymc3_vs_pystan


2. install remaining packages via pip (inc pymc3 master with deps):

        $> ./pip_install.sh


3. Launch Jupyter Notebook server

        $> jupyter notebook


---



# Data

Local data is not stored in the repo, and should be manually copied into the subdirectory data/

See file `data/README_DATA.md` for more info


---


# General Notes:

File `hack_findmap.py` contains a customised `find_MAP()` function to correct
for pymc3's default behaviour of computing gradients when the chosen optimizer
doesn't use them. We don't want to compute gradients in large datasets because it's
quite computationally expensive.

