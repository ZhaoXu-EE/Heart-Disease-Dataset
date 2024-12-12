# EE 475 Project Report: Machine Learning Model Development for Predicting Heart Disease Risk Using the UCI Heart Disease Dataset
Xu Zhao 12 Dec 2024

## 1. Introduction

This project leverages machine learning techniques to predict heart disease risk using medical features from the UCI Heart Disease dataset. By employing advanced algorithms and explainability tools, the study aims to enhance our understanding of heart disease predictors and improve diagnostic accuracy.

## 2. Dataset Overview

The UCI Heart Disease dataset, compiled from Cleveland, Hungary, Switzerland, and Long Beach V databases, contains 14 critical features related to heart health, such as age, cholesterol levels, and chest pain types. Categorical features were converted into numerical formats using one-hot encoding to facilitate model training.

## 3. Methodology

### 3.1 Dataset Preparation
- **Preprocessing**: 
  - Missing values were handled, and categorical features like chest pain type and fasting blood sugar were encoded into descriptive categories (e.g., "typical angina" or "lower than 120mg/ml").
  - The dataset was split into training and test subsets (80% and 20%, respectively).
  
### 3.2 Exploratory Data Analysis (EDA)
- Visualizations such as KDE plots, violin plots, and bar charts revealed patterns in age, maximum heart rate, and cholesterol distributions across disease classes.
- Heatmaps displayed correlations among features, highlighting relationships like the negative correlation between maximum heart rate and disease likelihood.

### 3.3 Model Development
- A Random Forest Classifier was chosen for its robustness in handling feature importance and ensemble learning.
  - **Hyperparameters**: Maximum tree depth of 5, 100 estimators.
  - Model training included rigorous cross-validation to optimize generalization.

### 3.4 Evaluation and Metrics
- Predictions on the test set were evaluated using precision, recall, F1-score, and ROC-AUC.
- Confusion matrices and ROC curves were plotted, demonstrating the model's ability to separate disease and non-disease cases effectively.

### 3.5 Explainability with SHAP
- SHAP values quantified each feature's contribution to predictions, providing insights into key predictors like maximum heart rate and chest pain type.
- Summary and dependence plots elucidated feature interactions, while force plots analyzed individual cases, showcasing model transparency.

## 4. Results

### 4.1 Model Performance
- The Random Forest model achieved an ROC-AUC score of 0.89, precision of 87%, and recall of 85%.
- Feature importance analysis ranked "maximum heart rate," "chest pain type," and "major vessels" as the top contributors to predictions.

### 4.2 Visual Insights
- Dependence plots revealed that higher maximum heart rates positively influenced disease predictions, while a higher number of major vessels reduced disease likelihood.
- Misclassified samples were examined using decision plots to refine the model further.

## 5. Key Findings
- **Feature Analysis**: SHAP identified maximum heart rate as a crucial factor, with a significant impact on predictions when combined with exercise-induced angina.
- **Misclassification Insights**: Decision plots showed that misclassifications often involved borderline cases with conflicting feature contributions.

## 6. Future Directions
- Integrating additional datasets with diverse demographics can improve model robustness.
- Experimenting with advanced architectures, such as gradient boosting or deep neural networks, may enhance accuracy.
- Real-world deployment for clinical validation can bridge the gap between research and healthcare applications.

## 7. Conclusion

This project successfully developed a machine learning model that provides accurate and interpretable predictions of heart disease risk. By leveraging SHAP and other visualization tools, the study bridges the gap between computational modeling and actionable healthcare insights.

## Appendix
Video Link:
https://www.canva.com/design/DAGZE9mNeLw/8ZkzQI1mWLrniRTcYzzkgQ/view?utm_content=DAGZE9mNeLw&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h6798d91764