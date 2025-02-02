# Rationalising data collection for supporting decision making in building energy systems using value of information analysis

This repository supports the article 'Rationalising data collection for supporting decision making in building energy systems using value of information analysis', published by the Journal of Building Performance Simulation on 5th Nov 2024. It is available online at [https://www.tandfonline.com/doi/full/10.1080/19401493.2024.2423827](https://www.tandfonline.com/doi/full/10.1080/19401493.2024.2423827).
It provides the code used to perform the Value of Information (VoI) calculations for the example problems presented in the paper.

## Technical Requirements

Use of this codebase requires Python 3.9 or later.
A suitable environment can be initialised using [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#) as follows:

```
conda create --name myenv python>=3.9
conda activate myenv
pip install -r requirements.txt
conda install -c conda-forge cmdstanpy
```

## Codebase Structure

This repository contains:

- Three scripts for performing the VoI calculations for each example problem:
    1. `building_ventilation.py`
    2. `ASHP_maintenance.py`
    3. `GSHP_design.py`
- `voi.py`, a generic implementation of the EVPI & EVII calculations for a general one-stage Bayesian decision problem (including accelerated versions).
- The `stan_models` directory, containing [Stan](https://github.com/stan-dev/stan) implementations of the probabilistic models used in the GSHP design example.
- The `data` directory, containing input data and cached utility evaluations for the GHSP design example.
- The `models` directory, containing an energy simulation model for the example GSHP system.
- The `results` directory, containing the numerical results of the sampling and evaluations used to perform the VoI calculations.
- The `plots` directory, containing code to produce the influence diagram figures for each example problem.
- The `trial_scipts` directory, containing scripts used for development and checking.
- A helpful caching function wrapper in `utils/caching.py`
