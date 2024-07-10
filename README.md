# HAZARD

Workflows template repository:

- [ ] Make sure to replace all occurrences of HAZARD (in the `README.md`, `environment.yml`, etc.) after copying this template.
- [ ] If possible, please use the package versions as specified in the environment.yml file of this template. We aim to keep a consistent enviroment throughout all CLIMAAX workflow repositories to allow for a seamless assessment of multiple hazards in a single environment. Nevertheless, please remove packages that are not used by workflows from the hazard repository's `environment.yml` file, but keep the `pip`, `jupyterlab`, `notebook`, `jupyterlab-myst` and `ipykernel` packages for convenience of the user.
- [ ] Only include a section on running with binder if the workflows actually start/run there.


Repository for collaboration on workflows for HAZARD hazard


## How to run

See our [how to run risk workflows](https://handbook.climaax.eu/CRA_steps/analysis/how_to.html) page in the CLIMAAX handbook for more information or follow the steps below:

### Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/CLIMAAX/HAZARD/main)


### Running locally

You may also download the repository from GitHub to run it locally:

1. Open your terminal

2. Check your conda install with `conda --version`. If you don't have conda, install it by following these instructions (see [here](https://docs.conda.io/en/latest/miniconda.html))

3. Clone the repository
    ```bash
    git clone git@github.com:CLIMAAX/HAZARD.git
    ```

4. Move into the cloned repository
    ```bash
    cd HAZARD
    ```

5. Create and activate your environment from the `environment.yml` file
    ```bash
    conda env create -f environment.yml
    conda activate climaax_HAZARD
    ```

6. Launch the jupyter interface of your preference, notebook, `jupyter notebook` or lab `jupyter lab`
7. Edit the notebook
8. Commit and push to the repo. **This step will be changed soon, introducing Pull Requests**.

These instructions were adapted from the [Environmental Data Science Book](https://edsbook.org/welcome.html) project.
