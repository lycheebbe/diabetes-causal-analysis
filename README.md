# 🧬 Causal Analysis of Diabetes Outcomes in Critical Care
## Overview

This repository presents a causal inference analysis examining the association between diabetes status and clinical outcomes among critically ill patients. The project focuses on cohort construction, confounding adjustment, and sensitivity analysis using modern causal inference methods commonly applied in biomedical and health research.

The goal of this repository is to demonstrate methodological reasoning and analytical workflow, rather than to provide a fully executable pipeline.

## Research Question

How is diabetes status associated with selected clinical outcomes among critically ill adult patients, after accounting for confounding factors?

Specifically, this project explores:

- Cohort definition and eligibility criteria

- Covariate balance before and after adjustment

- Estimation of adjusted effects using causal inference methods

- Robustness of findings through sensitivity analyses

## Data Source

This study used data from MIMIC-IV v3.1, a large, publicly available database containing de-identified health-related data associated with patients admitted to critical care units.

Access to the raw data requires:

- Completion of CITI training

- Credentialed access through PhysioNet

Due to data use agreements, raw data and executable SQL queries are not shared in this repository.

## Methods
### Cohort Construction

- Adult ICU admissions were identified using structured clinical tables

- Inclusion and exclusion criteria were applied to define the analytic cohort

- Baseline covariates included demographics, comorbidities, and clinical characteristics

The cohort construction logic is documented conceptually to ensure transparency while maintaining data compliance.

## Causal Framework

This analysis adopts a counterfactual causal inference framework, treating diabetes status as the exposure of interest and clinical outcomes as endpoints.

Key components include:

- Identification of potential confounders

- Adjustment using weighting-based methods

- Assessment of covariate balance

## Statistical Analysis

Analyses were conducted in R and include:

- Descriptive summaries of baseline characteristics

- Covariate balance diagnostics (e.g., standardized mean differences)

- Effect estimation using adjusted models

- Sensitivity analyses to assess robustness

## Key Results
### Covariate Balance

After confounding adjustment, covariate balance between exposure groups improved substantially.

(Example figure placeholder)

figures/balance_loveplot.png

### Effect Estimates

Adjusted models yielded interpretable estimates of the association between diabetes status and outcomes of interest.

(Example figure placeholder)

figures/effect_estimates.png

## Sensitivity Analysis

Sensitivity analyses were conducted to evaluate the stability of results under alternative modeling assumptions.

## Repository Structure

```r
├── README.md
├── analysis.Rmd
├── figures/
│   ├── balance_loveplot.png
│   ├── effect_estimates.png
│   └── sensitivity_analysis.png
└── sql/
    └── cohort_creation_pseudocode.sql
```

## Reproducibility Note

This repository is intended to document analytical logic and methodological decisions.

Because the analysis relies on restricted-access clinical data:

- Raw data are not included

- SQL queries are presented in pseudocode or descriptive form

- Full reproducibility requires independent credentialed access to MIMIC-IV

This approach aligns with standard practices in clinical and biomedical research.

## Intended Audience

This repository is designed for:

- Researchers interested in applied causal inference

- Graduate students and trainees in biostatistics or epidemiology

- Investigators seeking examples of transparent analytical workflows using restricted clinical data

## Disclaimer

This project was conducted for academic and methodological demonstration purposes.
All analyses use de-identified data and comply with applicable data use agreements.
