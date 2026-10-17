# UK Road Safety Data Preprocessing 2025

## Overview

This project applies a structured data preprocessing pipeline to the UK Road Safety Open Data 2025 published by the UK Department for Transport (DfT). It focuses on improving data quality, integrating related datasets, selecting relevant features, and reducing dimensionality for further analysis.

## Dataset

The project uses three datasets:

- **Collision:** Road collision records.
- **Vehicle:** Vehicles involved in reported collisions.
- **Casualty:** Casualties associated with reported collisions.

The datasets are supported by the official DfT Open Dataset Data Guide.

**Official source:** [UK Road Safety Open Data](https://www.gov.uk/government/statistical-data-sets/road-safety-open-data)

The data covers reported personal-injury road collisions on public roads in Great Britain. It should not be interpreted as representing every road collision.

## Preprocessing Pipeline

The project is organized into six stages:

1. **Data Understanding and Profiling** — Examine dataset structure, data types, missing values, duplicates, keys, and data granularity.
2. **Data Cleaning** — Identify and handle data quality issues based on evidence and documented variable definitions.
3. **Data Integration** — Integrate collision, vehicle, and casualty records while validating keys, relationships, and join cardinality.
4. **Redundancy Analysis and Feature Selection** — Examine potential redundancy and select relevant analytical features.
5. **Principal Component Analysis (PCA)** — Apply dimensionality reduction to suitable numerical features after appropriate scaling.
6. **Visualization and Evaluation** — Visualize preprocessing results and compare data conditions before and after processing.

Each stage includes validation checks to support reproducibility and maintain consistency throughout the pipeline.

## Tools and Technologies

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- seaborn
- scikit-learn

## Repository Contents

The repository contains Jupyter Notebooks documenting the preprocessing stages, including code, analysis, validation checks, and visualizations.

## Objectives

- Assess data quality and identify preprocessing requirements.
- Preserve data integrity during cleaning and integration.
- Identify potentially redundant features using statistical evidence.
- Reduce the dimensionality of selected numerical features using PCA.
- Document preprocessing decisions and evaluate the resulting data.

## Notes and Limitations

- Special values are interpreted according to the official data documentation rather than treated as missing values automatically.
- Outliers are investigated and are not removed solely because they fall outside typical ranges.
- Correlation is used as evidence of potential redundancy, not as an automatic feature-removal rule.
- PCA is applied only to suitable numerical analytical features, excluding identifiers.
- Results and conclusions are limited to the data and methods evaluated in this project.

## References

Department for Transport. *Road Safety Open Data.*

https://www.gov.uk/government/statistical-data-sets/road-safety-open-data

Han, J., Kamber, M., & Pei, J. *Data Mining: Concepts and Techniques* (3rd ed.). Morgan Kaufmann. Chapter 3: Data Preprocessing.
