# HAZARD

Repository for collaboration on workflows for HAZARD hazard.

[<img src="https://raw.githubusercontent.com/CLIMAAX/crabook/main/crabook/logo.png" height="100" />](https://climaax.eu)

Part of the [Climate Risk Assessment Handbook](https://handbook.climaax.eu/).


## How to run

See our [how to run risk workflows](https://handbook.climaax.eu/notebooks/workflows_how_to.html) page in the CLIMAAX handbook for more information.

### Launch a binder session

Binder sessions are not persistent and may not provide the necessary computing resources to run all workflow steps.

[![Binder](https://mybinder.org/badge_logo.svg)](INSERT-LINK-FOR-HAZARD-HERE-SEE-BELOW)

### Local setup with conda

```bash
# Clone the workflow repository
git clone https://github.com/CLIMAAX/HAZARD.git
cd HHAZARD

# Create a new environment and activate it
conda env create -f environment.yml

# Start the JupyterLab from within the created environment
conda activate climaax_HAZARD
jupyter lab
```

## How to contribute

See our [contributions](https://handbook.climaax.eu/community/contribute.html) page in the Handbook.

## License

`Apache-2.0 OR CC-BY-4.0` ([SPDX license identifier](https://spdx.dev/learn/handling-license-info/)).

## Acknowledgements

CLIMAAX has received funding from the European Union’s Horizon Europe – the Framework Programme for Research and Innovation (2021-2027) under grant agreement No. 101093864.




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
