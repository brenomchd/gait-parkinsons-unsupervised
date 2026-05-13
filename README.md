# Unsupervised Learning for Neurodegenerative Disease Analysis

This repository contains experiments developed at the **Human and Artificial Intelligence Laboratory (HAILab)** as part of an undergraduate research project focused on the application of **unsupervised machine learning methods** to the analysis of human gait data for the investigation of neurodegenerative diseases.

## 🧠 Motivation

Neurodegenerative diseases such as Parkinson’s disease, Huntington’s disease, and amyotrophic lateral sclerosis progressively affect the nervous system and significantly impact patients’ quality of life. Early diagnosis remains challenging and often depends on specialized clinical evaluation and expensive complementary exams.

Human gait represents a promising non-invasive biomarker, since alterations in walking patterns frequently emerge in early disease stages. Advances in wearable sensing technologies enable large-scale gait data collection, creating opportunities for computational analysis and discovery of clinically relevant patterns.

While most existing studies rely on supervised learning approaches, labeled biomedical datasets are often scarce. In this context, **unsupervised learning methods** offer an alternative strategy by allowing the identification of latent structures, clusters, and potential disease subtypes without requiring prior labeling.

## 🎯 Objectives

The main goal of this repository is to investigate the use of unsupervised learning techniques for:

* Exploration of gait datasets related to neurodegenerative conditions
* Extraction and aggregation of gait-derived features
* Dimensionality reduction for representation learning
* Clustering of subjects based on gait dynamics
* Evaluation of latent structures that may relate to disease characteristics or progression

## 📊 Dataset

Experiments currently use the [**Gait in Parkinson’s Disease Database (GaitPDB)**](https://www.physionet.org/content/gaitpdb/1.0.0/), which provides temporal gait signals collected from individuals with Parkinson’s disease and healthy controls.

## 📁 Repository Structure

```
.
├── data/            # Data organization
├── notebooks/       # Exploratory analysis and experimental workflows
├── results/         # Figures, tables, and experimental outputs
```

## 🔬 Methods

Current experiments include:

* Exploratory Data Analysis (EDA)
* Statistical aggregation of gait time-series
* Feature scaling and preprocessing
* Principal Component Analysis (PCA)
* K-Means clustering
* Internal and external clustering validation metrics

## 🚧 Project Status

This repository is part of an ongoing undergraduate research project. The codebase is under active development and will evolve as new experiments and methodologies are incorporated.

## 👨‍💻 Author

**Breno Machado Barros**
Undergraduate Researcher — HAILab
Institute of Informatics - UFG

## 🤝 Acknowledgements

* Prof. Dr. Juliana Paula Félix & Prof. Dr. Rogério Lopes Salvini
* Public biomedical datasets enabling reproducible research
