# NHANES_-Analysis


# Survey-Weighted Diabetes Risk Prediction Using NHANES (2005–2018)

## Overview

This repository accompanies a research study investigating the incremental predictive value of routinely measured laboratory biomarkers for identifying undiagnosed diabetes in U.S. adults using the National Health and Nutrition Examination Survey (NHANES).

The study integrates complex survey design considerations, stability-based laboratory marker selection, temporal evaluation, calibration assessment, and decision curve analysis.

The primary objective is to assess whether a parsimonious laboratory panel can improve risk prediction beyond routinely available clinical characteristics.

## Data Source

**National Health and Nutrition Examination Survey (NHANES), 2005–2018**

- Data provider: National Center for Health Statistics (NCHS), Centers for Disease Control and Prevention (CDC).
- Study population: Adults aged 20 years and older without previously reported diabetes or borderline diabetes.
- Analytic sample: 14,433 participants.
- Development period: 2007–2016.
- Temporal evaluation period: 2017–2018.
- Sensitivity analysis: Inclusion of the 2005–2006 cycle in model development.

NHANES data are publicly available through the [CDC NHANES website](https://www.cdc.gov/nchs/nhanes/).

## Methodology

The analytical framework consists of:

1. Data integration and preprocessing across NHANES survey cycles.
2. Glucose harmonization and definition of undiagnosed diabetes.
3. Survey-aware model development using clinical predictors.
4. Stability-based selection of laboratory biomarkers.
5. Comparison of clinical-only, selected-laboratory, and full-laboratory models.
6. Temporal evaluation using the 2017–2018 NHANES cycle.
7. Assessment of discrimination, calibration, and clinical net benefit.
8. Sensitivity analyses and uncertainty estimation using survey-design considerations.

## Prediction Models

Three predictive strategies were evaluated:

| Model | Description |
|---|---|
| Clinical | Clinical and demographic predictors |
| Selected laboratory | Clinical predictors supplemented with four selected laboratory biomarkers |
| Full laboratory | Clinical predictors supplemented with the complete candidate laboratory panel |

The selected laboratory biomarkers were triglycerides, gamma-glutamyltransferase (GGT), total protein, and HDL cholesterol.

## Main Results

Survey-weighted performance in the 2017–2018 temporal evaluation sample:

| Model | AUROC | AUPRC | Brier score |
|---|---:|---:|---:|
| Clinical | 0.7813 | 0.1178 | 0.03918 |
| Selected laboratory | 0.7988 | 0.1383 | 0.03791 |
| Full laboratory | 0.8156 | 0.1579 | 0.03745 |

The full laboratory panel improved AUROC relative to the clinical model by approximately 0.034, with an approximate 95% confidence interval of 0.016–0.055.

These results indicate improvements in discrimination, while calibration and clinical utility require separate consideration.

## Reproducibility

The repository is intended to provide the analytical code and supporting materials used in the study.

NHANES source data are publicly available from the CDC and are not redistributed here. Users should download the relevant survey-cycle files directly from the official source.

The analysis incorporates survey weights, strata, and primary sampling units. Bootstrap confidence intervals based on fixed predictions do not fully capture model-development uncertainty.

## Limitations

- Temporal evaluation was conducted using a subsequent NHANES survey cycle rather than an independent clinical cohort.
- Laboratory measurements and harmonization procedures require careful consideration across survey cycles.
- Subgroup analyses are exploratory.
- The findings do not establish clinical effectiveness or justify deployment without additional validation.

## Citation

If you use this repository, please cite the accompanying manuscript once its bibliographic information becomes available.

## License

No license has been specified. Please refer to the repository's license file if one is subsequently added.
