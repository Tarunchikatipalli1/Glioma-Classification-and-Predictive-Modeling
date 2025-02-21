# Glioma Grading Prediction

This R Markdown project performs predictive modeling for glioma grading (LGG vs. GBM) using clinical and molecular features, comparing k-NN, Naive Bayes, and Decision Tree models.

## Overview
This project provides a comprehensive analysis pipeline for predicting glioma grades (Low-Grade Glioma or Glioblastoma Multiforme) using the UCI Glioma Grading dataset. Built in R Markdown, it includes data preprocessing, exploratory data analysis, feature engineering, and model evaluation, all within a single reproducible file.

## Features
- Upload and process the UCI Glioma Grading dataset (clinical and mutation features).
- Perform data preprocessing (normalization, log transformation, PCA).
- Generate visualizations (UMAP, correlation plots, ROC curves).
- Train and evaluate three classification models: k-NN, Naive Bayes, Decision Trees.
- Export results and visualizations.

## Installation
To run the project locally, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Tarunchikatipalli1/Glioma-Grading-Prediction.git
   cd Glioma-Grading-Prediction
   ```
   
3. **Open R and install required dependencies if not already installed:**
   ```bash
   install.packages(c("rpart", "rpart.plot", "readr", "archive", "ggplot2", "corrplot", "dplyr", "MASS", "caret", "class", "e1071", "glmnet", "pROC", "tinytex"))
   ```


5. **Download the datasets:**
   - Place TCGA_GBM_LGG_Mutations_all.csv and TCGA_InfoWithGrade.csv in the /data folder.
   - Alternatively, download from UCI Repository: https://archive.ics.uci.edu/ml/datasets/Glioma+Grading+Clinical+and+Mutation+Features

6. **Run the analysis:**
   ```bash
   library(rmarkdown)
   render("docs/report.Rmd")
   ```

## How to Use This Project
1. **Prepare the Data:**
   - Ensure the datasets are in the /data folder with paths correctly specified in report.Rmd.

2. **Run the Analysis:**
   - Open docs/report.Rmd in RStudio and click "Knit" to execute the full pipeline.
   - Alternatively, use the command above to render the file.

3. **Explore Results:**
   - View UMAP plots, correlation matrices, and ROC curves in the output (HTML or PDF).
   - Check model performance metrics (Accuracy, Precision, Recall, F1 Score, ROC-AUC).

4. **Download Results:**
   - Visualizations and results are embedded in the rendered output for easy export.

## File Structure
- **docs/report.Rmd**: Single R Markdown file containing the full analysis pipeline (data loading, preprocessing, modeling, and visualization).
- **/data/**: Folder for datasets:
  - **TCGA_GBM_LGG_Mutations_all.csv**: Raw clinical and mutation data.
  - **TCGA_InfoWithGrade.csv**: Preprocessed numeric data.
- **README.txt**: This file with project overview and instructions.

## Key Results

| Model         | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---------------|----------|-----------|--------|----------|---------|
| k-NN          | 0.9702   | 0.98      | 0.9703 | 0.9751   | 0.9702  |
| Naïve Bayes   | 0.8333   | 0.9506    | 0.7624 | 0.8462   | 0.8513  |
| Decision Tree | 1.0      | 1.0       | 1.0    | 1.0      | 0.8513  |

- **Best Model**: k-NN offers balanced performance.
- **Note**: Decision Tree's perfect scores may indicate overfitting.

## Acknowledgments
This project leverages the following R packages:
- **Seurat**: For data processing (inspiration from scRNA-seq workflows).
- **caret, e1071, rpart**: For machine learning models.
- **ggplot2, corrplot, pROC**: For visualizations.

## License
This project is open-source and available under the MIT License.

## About
Developed by Tarun Chikatipalli as a predictive modeling exercise for glioma grading. No additional website or topics provided.

Resources
- **UCI Glioma Grading Dataset:**
- **R Markdown Documentation:**
- **GitHub Repository**


(c) 2025 GitHub, Inc.
Footer Navigation: Terms | Privacy | Security | Status | Docs | Contact
