# Diabetes-Predictions-ML

Diabetes Risk Prediction Using Machine Learning

A supervised machine learning project focused on estimating diabetes risk through classification models, preprocessing, model comparison, threshold-based evaluation, and model explainability.

Repository: Diabetes-Predictions-ML
Notebook: diabetes-predictions.ipynb
Kaggle Notebook: Diabetes Predictions
Portfolio: Hassan Farid — Portfolio

⸻

1. Project Overview

This project applies machine learning classification techniques to diabetes risk prediction. It investigates how preprocessing decisions, model selection, classification thresholds, and model explainability influence predictive performance.

Two classification algorithms were compared:

* Logistic Regression
* Random Forest

The project evaluates model performance using cross-validation and a separate held-out evaluation. It also incorporates SHAP-based analysis to support the interpretation of model predictions.

The objective is to develop and evaluate a structured machine learning workflow while examining the trade-offs between predictive discrimination and classification performance.

2. Project Objectives

The main objectives are to:

* Develop a reproducible machine learning workflow for diabetes risk prediction.
* Identify and handle implausible zero values in relevant features.
* Compare Logistic Regression and Random Forest.
* Evaluate model performance using appropriate classification metrics.
* Examine the effect of classification threshold selection.
* Apply explainability techniques to investigate model behaviour.
* Discuss the limitations of machine learning predictions in a healthcare-related context.

3. Technical Highlights

* Data preprocessing: Treated implausible zero values as missing observations where appropriate.
* Pipeline-based processing: Integrated preprocessing and modelling to reduce the risk of data leakage during cross-validation.
* Model comparison: Evaluated Logistic Regression and Random Forest using cross-validation ROC-AUC.
* Threshold evaluation: Examined a selected classification threshold of 0.417 for the Random Forest evaluation.
* Model explainability: Used SHAP-based analysis to investigate model explanations.
* Evaluation discipline: Reported cross-validation and held-out results separately rather than treating them as directly interchangeable.

4. Methodology

The workflow is organised around the following stages.

4.1 Data preparation

The dataset was examined and prepared for machine learning.

A key preprocessing decision involved identifying zero values that were considered implausible for relevant measurements and treating them as missing values.

Imputation was incorporated into modelling pipelines rather than being performed indiscriminately before cross-validation. This helps ensure that preprocessing is learned within the relevant training folds.

4.2 Model development

Two classification approaches were evaluated:

Model	Approach
Logistic Regression	Linear classification baseline
Random Forest	Ensemble-based tree classification

4.3 Model evaluation

Cross-validation ROC-AUC was used to compare the models’ ability to distinguish between the target classes.

The Random Forest model was also assessed on held-out data using several classification metrics.

The evaluation included threshold-based predictions rather than relying exclusively on a default classification threshold.

4.4 Explainability

SHAP-based analysis was used to examine model explanations.

The analysis is intended to provide additional insight into model behaviour. Feature-level conclusions should be drawn from the actual SHAP outputs and interpreted in the context of the dataset.

5. Model Performance and Results

5.1 Cross-validation comparison

Model	Mean ROC-AUC	Standard deviation
Logistic Regression	0.844	0.016
Random Forest	0.836	0.021

Interpretation

Logistic Regression achieved a slightly higher mean cross-validation ROC-AUC than Random Forest.

The difference is relatively small. These results alone do not establish that one model is statistically superior to the other.

5.2 Random Forest held-out evaluation

Metric	Result
ROC-AUC	0.82
Accuracy	75%
Precision	60%
Recall	81%
Specificity	71%
Selected threshold	0.417

Interpretation

The reported Random Forest evaluation demonstrates a recall-oriented classification outcome:

* Recall of 81%: The model identified 81% of the actual positive cases in the evaluated sample.
* Precision of 60%: Of the cases predicted as positive, 60% were actually positive.
* Specificity of 71%: The model correctly identified 71% of the actual negative cases.
* Accuracy of 75%: Overall, 75% of evaluated predictions were correct.
* ROC-AUC of 0.82: The model demonstrated discriminatory ability in the held-out evaluation.

The selected threshold of 0.417 represents a threshold-based classification decision. It should not be interpreted as a clinically established decision boundary.

Evaluation note: The cross-validation results and held-out Random Forest results represent different evaluation stages. They should not be compared as though they were obtained from the same evaluation sample.

6. Key Findings

1. Logistic Regression achieved the higher mean cross-validation ROC-AUC among the two evaluated models.
2. Random Forest achieved a held-out ROC-AUC of 0.82.
3. The selected Random Forest threshold produced a recall of 81%, alongside a precision of 60%.
4. Handling implausible zero values as missing observations was an important preprocessing consideration.
5. SHAP analysis provided an explainability component to complement predictive performance evaluation.

7. Repository Structure

The repository currently contains the following files:

Diabetes-Predictions-ML/
│
├── README.md
│
└── diabetes-predictions.ipynb

File	Description
README.md	Project overview, methodology, results, and documentation.
diabetes-predictions.ipynb	Main Jupyter Notebook containing the project analysis and modelling workflow.

There are no separate data, source-code, or dependency folders in the current repository root.

8. How to Explore and Run the Project

Option 1: Explore on GitHub

1. Open the GitHub repository.
2. Select diabetes-predictions.ipynb.
3. Review the notebook cells, methodology, outputs, and available visualisations.

GitHub displays notebooks as static rendered content. Some interactive notebook features may not work in this view.

Option 2: Run on Kaggle

The Kaggle notebook is the recommended starting point for an interactive execution environment.

1. Open the Diabetes Predictions Kaggle Notebook.
2. Sign in to Kaggle if required.
3. Open the notebook.
4. Use Kaggle’s available notebook execution options to run the cells in sequence.
5. Review the preprocessing, model comparison, evaluation outputs, and explainability analysis.

Local execution

The repository currently contains the notebook but no separate requirements.txt or dataset file in its root directory.

For local execution, review the notebook’s import and data-loading cells first. Install the required dependencies and make the dataset available at the location expected by the notebook.

9. Reproducibility and Evaluation Considerations

For a meaningful review of the experiment:

* Execute notebook cells in their intended order.
* Review the data-loading and preprocessing steps before interpreting results.
* Check the cross-validation and held-out evaluation sections independently.
* Confirm the selected threshold when examining classification metrics.
* Review the SHAP outputs before making feature-level interpretations.

The repository does not currently include a separate dependency lockfile or a standalone data directory. The notebook is the primary record of the implementation.

10. Limitations

* Predictive performance depends on the dataset and the observations represented in it.
* The reported metrics do not establish clinical validity.
* A classification threshold selected during experimentation is not automatically appropriate for real-world medical decisions.
* The difference in cross-validation ROC-AUC does not establish statistical significance.
* Model explanations should not be interpreted as evidence of causation.
* Independent validation on additional populations and datasets would be required before considering any real-world healthcare application.

Disclaimer: This project is for educational and analytical purposes only. It is not a clinically validated diagnostic system and must not be used to diagnose diabetes or make medical decisions.

11. Future Improvements

Potential areas for further development include:

* More extensive hyperparameter optimisation.
* Additional model comparisons.
* Calibration analysis for predicted probabilities.
* Further threshold sensitivity analysis.
* External validation using independent datasets.
* More detailed interpretation of SHAP results.
* Stronger experiment tracking and dependency documentation.

12. Author and Project Links

Hassan Farid
Data Science | Machine Learning | Artificial Intelligence

* GitHub Profile
* Kaggle Profile
* LinkedIn
* Portfolio

⸻

This repository documents an applied machine learning project, including data preparation, model comparison, evaluation, and explainability considerations.
