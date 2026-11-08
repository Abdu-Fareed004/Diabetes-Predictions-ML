# Diabetes-Predictions-ML

Diabetes Prediction Using Machine Learning

Project Overview

This project applies machine learning techniques to predict the likelihood of diabetes using patient-related health indicators. It explores data preprocessing, model development, cross-validation, threshold selection, performance evaluation, and model interpretability.

-Project Repository: [Diabetes Predictions ML](https://github.com/Abdu-Fareed004/Diabetes-Predictions-ML)
-- Kaggle Notebook: [View Diabetes Predictions on Kaggle](https://www.kaggle.com/code/fareedhassan/diabetes-predictions)

The objective is to investigate how machine learning classification
models can support risk prediction and provide a structured comparison of their predictive performance.

Project Objectives

* Examine and preprocess the dataset for machine learning.
* Handle implausible zero values in relevant health measurements as missing observations.
* Build and evaluate classification pipelines.
* Compare Logistic Regression and Random Forest using cross-validation.
* Evaluate the selected Random Forest model on a held-out evaluation set.
* Explore model interpretability using SHAP.

Technical Highlights

* Data preprocessing: Identified implausible zero values and treated them as missing observations.
* Pipeline-based imputation: Applied imputation within machine learning pipelines to integrate preprocessing with model evaluation.
* Model comparison: Evaluated Logistic Regression and Random Forest using cross-validation.
* Threshold selection: Examined classification performance using a selected probability threshold of 0.417.
* Model interpretability: Used SHAP analysis to investigate model predictions.

Machine Learning Workflow

1. Data inspection and exploratory analysis.
2. Identification and treatment of missing or implausible values.
3. Preprocessing and imputation.
4. Model development using Logistic Regression and Random Forest.
5. Cross-validation and model comparison.
6. Held-out evaluation of the Random Forest model.
7. Threshold-based classification analysis.
8. SHAP-based model interpretation.

Model Performance

Cross-validation Results

Model	Mean ROC-AUC	Standard Deviation
Logistic Regression	0.844	0.016
Random Forest	0.836	0.021

Logistic Regression achieved a slightly higher mean ROC-AUC than Random Forest during cross-validation. The difference is relatively small and should not be interpreted as evidence of statistically significant superiority.

Random Forest Held-out Evaluation

Metric	Result
ROC-AUC	0.82
Accuracy	75%
Precision	60%
Recall	81%
Specificity	71%
Selected Threshold	0.417

Results Interpretation

The Random Forest model achieved a recall of 81%, indicating that it identified a substantial proportion of positive cases in the evaluated data.

Its precision of 60% indicates that some positive predictions were false positives. This illustrates the importance of considering the trade-off between identifying positive cases and limiting false-positive predictions.

The selected threshold of 0.417 represents the probability threshold used for the reported classification metrics.

Cross-validation and held-out evaluation results represent different evaluation stages and should be interpreted separately.

Model Interpretability

SHAP analysis was incorporated to examine how input variables contribute to model predictions.

This provides an additional interpretability layer beyond aggregate performance metrics. The analysis is intended to support investigation of model behaviour, not to establish causal relationships between health indicators and diabetes.

Repository Structure

The repository contains the following files:

Diabetes-Predictions-ML/
├── README.md
└── diabetes-predictions.ipynb

File	Description
README.md	Project overview, methodology, results, and documentation.
diabetes-predictions.ipynb	Main Jupyter Notebook containing data analysis, preprocessing, model development, evaluation, and interpretability.

Access the Project

* GitHub Repository: Diabetes Predictions ML
* GitHub Notebook: View the Jupyter Notebook
* Kaggle Notebook: Explore Diabetes Predictions on Kaggle

How to Explore the Project

1. Open the GitHub repository.
2. Select diabetes-predictions.ipynb from the repository’s root directory.
3. Review the notebook sections to follow the analytical workflow.
4. Alternatively, open the Kaggle Notebook to explore the analysis in an interactive notebook environment.

Limitations and Future Improvements

Potential areas for further development include:

* More extensive hyperparameter optimisation.
* Additional classification algorithms and ensemble comparisons.
* Calibration of predicted probabilities.
* Further investigation of threshold selection and its operational implications.
* More comprehensive model validation on independent datasets.
* Deeper investigation of model explanations and feature contributions.

Disclaimer

This is an educational and analytical machine learning project. The model has not been clinically validated and must not be used as a substitute for professional medical assessment, diagnosis, or treatment.

## Author

**Hassan Farid**

Data Science | Machine Learning | Artificial Intelligence

- Portfolio: [Visit My Portfolio](https://v0-farid-portfolio-updated.vercel.app/)
- GitHub: [Visit My GitHub](https://github.com/Abdu-Fareed004)
- Kaggle: [Visit My Kaggle](https://www.kaggle.com/fareedhassan)
- LinkedIn: [Connect on LinkedIn](https://www.linkedin.com/in/hassan-farid-99b9013b1)
- Twitter/X: [Follow Me on X](https://x.com/therealfareed_4)
- Instagram: [Follow Me on Instagram](https://www.instagram.com/thereal_fareed)

