# Investigation of Unsupervised Methods to Support the Diagnosis of Neurodegenerative Diseases Through Gait Analysis

This repository contains the experiments developed in an undergraduate research project focused on human gait analysis using unsupervised machine learning techniques, with an initial emphasis on Parkinson’s disease.

The project investigates whether latent biomechanical patterns can be identified from gait signals, contributing to the understanding of motor alterations associated with neurodegenerative diseases and to the future development of computational tools for clinical analysis support.

## Context and Motivation

Neurodegenerative diseases may produce progressive alterations in motor control, often observable in gait. Because gait is a functional, repetitive, and measurable activity, it represents a promising biomarker for computational studies of neurological disorders.

A substantial part of the literature relies on supervised approaches, which depend on previously defined clinical labels. In this project, the use of unsupervised methods enables the exploration of the intrinsic structure of the data and the investigation of biomechanical groupings without imposing prior classes, preserving room for the discovery of locomotor profiles that may not yet be evident.

## Objective

To identify latent biomechanical gait patterns in data from individuals with Parkinson’s disease and healthy controls using unsupervised learning techniques, with emphasis on biomechanical interpretability.

## Dataset

The experiments use the public **Gait in Parkinson’s Disease Database (GaitPDB)**, made available by PhysioNet.

The dataset contains temporal vertical force signals collected under different experimental gait protocols, including:

- baseline walking;
- cognitive interference;
- rhythmic auditory stimulation;
- treadmill walking.

## Repository Structure

```text
.
├── data/                         # Raw files and organized data
├── notebooks/                    # Exploratory analyses and initial notebooks
├── experiments/
│   ├── baseline/                 # Experiments with baseline conditions
│   └── protocol_analysis/        # Analyses by experimental protocol
├── results/                      # Figures, tables, and experimental outputs
└── README.md
```

## Experimental Pipeline

The current analysis workflow follows the sequence:

```text
Raw gait signals (.txt)
        ↓
Biomechanical feature extraction
        ↓
Data normalization
        ↓
PCA visualization
        ↓
K-Means clustering
        ↓
Cluster evaluation
        ↓
Biomechanical interpretation
```

## Biomechanical Features

The current experiments use statistical features extracted separately for the left and right feet, together with asymmetry measures:

- `mean_total_L`
- `mean_total_R`
- `std_total_L`
- `std_total_R`
- `cv_total_L`
- `cv_total_R`
- `assimetria_mean`
- `assimetria_abs`
- `peak_force_L`
- `peak_force_R`

These features were selected because they combine simplicity, reproducibility, and biomechanical relevance, allowing clearer interpretation of the identified clusters.

## Implemented Methods

- `StandardScaler`
- `PCA`
- `K-Means`
- `Silhouette Score`
- `Davies-Bouldin Index`
- `Calinski-Harabasz Score`

## Experimental Studies

### 1. Ga Protocol — Cognitive Interference

Analyzed conditions:

- `Ga01` — baseline walking;
- `Ga02` — simple task;
- `Ga10` — arithmetic task.

### 2. Ju Protocol — Rhythmic Auditory Stimulation

Analyzed conditions:

- `Ju01` — baseline condition;
- `Ju02` — RAS 100%;
- `Ju03` — carryover 1;
- `Ju04` — RAS 110%;
- `Ju05` — carryover 2;
- `Ju06` — carryover 3;
- `Ju07` — dual task.

### 3. Si Protocol — Treadmill Walking

Study designed to analyze locomotor patterns under treadmill walking conditions.

## Main Findings So Far

The experiments conducted to date indicate that:

- rhythmic auditory stimulation improves the structural organization of gait clusters;
- the `RAS 110%` condition produces high biomechanical heterogeneity;
- carryover conditions reveal distinct locomotor adaptation profiles;
- dual-task conditions tend to reduce cluster separability;
- gait asymmetry consistently emerges as a relevant biomechanical factor.

These results should still be interpreted within the exploratory scope of the project, but they already suggest that different experimental conditions modulate the latent structure of gait in distinct ways.

## Experiment Organization

The experiments are maintained in modular notebooks containing:

- explicit definition of objectives;
- methodological justification;
- commented code blocks;
- quantitative evaluation of clustering results;
- biomechanical interpretation of findings.

The project prioritizes scientific traceability and avoids unnecessary methodological complexity before consolidating the fundamental patterns present in the data.

## Project Status

Ongoing project. The next steps include expanding the comparative analysis across protocols, consolidating the biomechanical interpretation of clusters, and progressively improving the documentation of the experiments.

## Author

Breno Machado Barros

## Acknowledgements

- Prof. Dr. Juliana Paula Félix
- Prof. Dr. Rogério Lopes Salvini
- PhysioNet, for making the dataset publicly available
