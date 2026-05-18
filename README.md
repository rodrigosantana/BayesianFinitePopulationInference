# Bayesian Finite Population Inference

This repository contains **R code for Bayesian finite population inference workflows** with a focus on generating and using synthetic finite populations for simulation studies, method development, and inferential validation.

## What this project is for

Finite population inference differs from superpopulation-only analyses because the target is a **fixed, finite set of units**. In practice, analysts often have only sample-level observations and partial auxiliary information. This project supports workflows where you:

1. Define or load a finite target population structure.
2. Generate synthetic populations under user-specified assumptions.
3. Draw samples according to a sampling design.
4. Fit Bayesian models to sampled data.
5. Estimate finite-population quantities (totals, means, proportions, subgroup estimates, etc.) with uncertainty.

## Core capabilities

- **Synthetic population generation** for controlled experiments.
- **Design-aware sampling simulations** (e.g., simple random sampling or other implemented designs).
- **Bayesian model-based inference** for finite-population estimands.
- **Uncertainty quantification** through posterior summaries and interval estimates.
- **Reproducible experimentation** by scripting end-to-end pipelines in R.

## Typical workflow

1. **Set parameters** for population size, covariate distributions, and outcome mechanisms.
2. **Generate synthetic population data**.
3. **Select samples** from the finite population using a chosen design.
4. **Fit Bayesian inference model(s)** on observed sample data.
5. **Project to finite-population estimands** and compute posterior summaries.
6. **Evaluate performance** (bias, coverage, RMSE, calibration) across repeated simulations.

## Illustration

```mermaid
flowchart LR
    A[Define finite population setup] --> B[Generate synthetic finite population]
    B --> C[Draw sample under sampling design]
    C --> D[Fit Bayesian model]
    D --> E[Infer finite-population quantities]
    E --> F[Summarize posterior uncertainty]
    F --> G[Evaluate simulation performance]
```

## Suggested repository usage

- Place raw and intermediate data in clearly separated directories.
- Keep model-fitting scripts modular (data prep, modeling, diagnostics, reporting).
- Fix random seeds for reproducibility in simulation studies.
- Record simulation settings and package versions alongside outputs.

## Requirements

- **R** (recent version recommended)
- R packages required by the project scripts (install as needed)

## Citation

If you use this repository in research or teaching, please cite the project and describe your simulation assumptions (population generation, sampling design, and Bayesian model specification) for reproducibility.
