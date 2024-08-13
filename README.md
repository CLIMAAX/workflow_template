# HAZARD

Repository for collaboration on workflows for HAZARD hazard.

[<img src="https://raw.githubusercontent.com/CLIMAAX/crabook/main/crabook/logo.png" height="100" />](https://climaax.eu)

Part of the [Climate Risk Assessment handbook](https://handbook.climaax.eu/).


## How to run

See our [how to run risk workflows](https://handbook.climaax.eu/notebooks/workflows_how_to.html) page in the CLIMAAX handbook for more information.

### Launch a binder session

Binder sessions are not persistent and may not provide the necessary computing resources to run all workflow steps.

[![Binder](https://mybinder.org/badge_logo.svg)](INSERT-LINK-FOR-HAZARD-HERE-SEE-BELOW)

### Quickstart: local setup

In a terminal where git and conda are available:

1.  Clone the repository

        git clone git@github.com:CLIMAAX/HAZARD.git

2.  Move into the cloned repository

        cd HAZARD

3.  Create a new environment from the `environment.yml` file

        conda env create -f environment.yml

4.  Activate the environment

        conda activate climaax_HAZARD

5.  Launch the Jupyter interface of your preference with

        jupyter lab

    or

        jupyter notebook


## How to contribute

See our [contribute to risk recipes](https://handbook.climaax.eu/community/contribute.html) page in the handbook for more information.



## Developer information

Things to consider when setting up a new workflow repository. *Delete this section of the README after setting up.*

### Insert name of hazard

Make sure to replace all occurrences of HAZARD (in the `README.md`, `environment.yml`, etc.) with the name of your hazard (e.g. hail) after copying this template.

### Conda environment

- Use the **package versions** as specified in the `environment.yml` file provided with the template.
  We aim to keep a consistent enviroment throughout all CLIMAAX workflow repositories to allow for a seamless assessment of multiple hazards in a single environment.
  Packages are installed from the [conda-forge](https://conda-forge.org/) channel.

- Please **remove packages** that are not used by your workflows from your new hazard repository's `environment.yml` file to keep the hazard-specific environment as light as possible, but *always* keep the ipykernel, jupyterlab-myst, jupyterlab, notebook and pip packages for the convenience of the user.

- We **only explicitly specify packages** that are directly imported in the workflows and some optional dependencies of these packages.
  E.g., dask and netcdf4 should be specified whenever xarray is used to load NetCDF files so `xarray.open_mfdataset` works, even if the dask and netcdf4 packages are not imported directly in any of the workflow notebooks.
  In contrast, instead of specifying a version for matplotlib-base explicitly, we only specify a version for matplotlib and let conda resolve the dependency.

- To **add a package to the environment** of an existing workflow repository, pick its version from the general `environment.yml` file in the template repository.
  If the package doesn't exist in the general environment yet, find a compatible version and open a [pull request](https://github.com/CLIMAAX/workflow_template/pulls) or [issue](https://github.com/CLIMAAX/workflow_template/issues) in the template repository so it can be added to the general environment.
  A way to select a compatible version is to first create the workflow or general environment without the new package, then install the package(s) without specifying a version and using the version that is automatically installed (conda will pick a compatible version if possible).

### Binder link

Binder sessions should be launched via the [CLIMAAX/binder-env](https://github.com/CLIMAAX/binder-env) repository, pulling the workflow repository content in with nbgitpuller.
Instructions for creating a link to launch binder in this way are provided in the binder-env repository.
