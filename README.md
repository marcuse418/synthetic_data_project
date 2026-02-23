# Synthetic Data Generation and Evaluation Research

This repository contains a research project focused on the generation, validation, and utility analysis of synthetic data. The project explores methods to create high-fidelity synthetic datasets that maintain the statistical properties of real-world data while providing privacy-preserving alternatives for research and development.

## Project Overview

As data privacy regulations (like GDPR and CCPA) become more stringent, synthetic data has emerged as a critical tool for data scientists. This project investigates the "fidelity-utility-privacy" tradeoff by:

1. Generating synthetic versions of a source dataset using advanced modeling techniques.
2. Evaluating Fidelity by comparing statistical distributions and correlations between real and synthetic data.
3. Assessing Utility by training machine learning models on synthetic data and testing them on real-world holdout sets.

## Key Features

- **Data Preprocessing:** Comprehensive cleaning and encoding pipeline for categorical and numerical features.
- **Generation Engine:** Implementation of synthetic data generators (utilizing libraries such as SDV - Synthetic Data Vault).
- **Statistical Validation:**
  - Distribution analysis (histograms and density plots).
  - Correlation matrix comparisons.
  - Cumulative Distribution Function (CDF) matching.
- **ML Utility Testing:** Comparison of model performance (Accuracy, F1-Score, ROC-AUC) when trained on real vs. synthetic data.

## Technologies Used
- Python
- Pandas/NumPy
- Matplotlib/Seaborn
- Scikit-learn
- SDV (Synthetic Data Vault)

## Getting Started
### Prerequisites
Ensure you have a Python environment set up. You can install the necessary dependencies using pip:
```python
pip install pandas numpy matplotlib seaborn scikit-learn sdv
```

### Running the Notebook
1. Clone the repository to your local machine.
2. Open the Jupyter Notebook
3. Run the cells sequentially to observe the data generation process and the subsequent evaluation metrics.

## Methodology
### Data Synthesis
The project employs probabilistic modeling to capture the underlying structure of the original data. This includes handling complex relationships between variables and ensuring data types are preserved.

### Fidelity Evaluation
We measure how well the synthetic data mimics the real data. This involves comparing:
- **Column Shapes:** Do the individual variables have the same mean, variance, and range?
- **Column Pairwise Trends:** Are the correlations between variables preserved?

### Utility Analysis
A "Train on Synthetic, Test on Real" (TSTR) approach is used to verify if the synthetic data can be used as a drop-in replacement for training predictive models without significant loss in performance.

## Conclusion and Findings

The research indicates that while synthetic data successfully captures primary statistical distributions, complex multi-variate correlations present a greater challenge. The ML utility tests provide a benchmark for how much "signal" is successfully transferred from the real dataset to the synthetic one.

*Developed as part of a research initiative into Privacy-Enhancing Technologies (PETs).*




