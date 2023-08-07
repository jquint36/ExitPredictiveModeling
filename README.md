# ExitPredictiveModeling

This repository contains an in-depth exploration and modeling of a dataset related to customer churn. The main objective is to predict whether a customer will exit or not. The work is data-driven, with methodologies ranging from data cleaning to advanced machine learning techniques. It's intended for both educational and practical purposes.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Exploration and Cleaning](#data-exploration-and-cleaning)
- [Modeling and Evaluation](#modeling-and-evaluation)
- [Results and Discussion](#results-and-discussion)
- [Conclusions and Recommendations](#conclusions-and-recommendations)
- [Future Work](#future-work)
- [Contributing and Feedback](#contributing-and-feedback)

## Project Overview

The aim of this project is to analyze a dataset containing customer details and their behaviors to predict customer churn. The goal is to build a predictive model that is both accurate and interpretable, aiding businesses in understanding and potentially mitigating customer exits.

## Data Exploration and Cleaning

- Initial inspection of data headers and shape.
- Checked data types and class distribution.
- Outlier detection and visualization.
- Segmentation and visualization, including age distribution, complaint frequency, salary distribution, etc.
- Removed irrelevant features such as surnames and customer ID.

## Modeling and Evaluation

The modeling phase was extensive and iterative:

- **Features Used**: Initially ['Complain', 'Age', 'IsActiveMember', 'Balance', 'NumOfProducts'] and later changed from Complain to Credit Score.
- **Models Employed**: Logistic Regression, Random Forest, XGBoost.
- **Techniques Applied**: Standard scaling, 10-fold cross-validation, hyperparameter tuning, and SMOTE for handling class imbalance.

## Results and Discussion

### Initial Findings with 'Complain' feature:

- The 'Complain' feature played an overwhelmingly influential role in the initial high scores. XGBoost and Random Forest showed an accuracy of around 98%.

### Why Exclude 'Complain'?

Our SHAP analysis revealed that the 'Complain' feature had a disproportionately high influence. While achieving high accuracy is vital, ensuring that the model is versatile and not overly dependent on one feature is crucial for real-world applications.

### - Subsequent Iterations: 

After removing the dominant 'Complain' feature, several other models were tested to optimize accuracy and ensure real-world applicability. The results from these iterations, while not as high as the initial models, were still promising and, more importantly, were based on a broader range of features making them potentially more reliable in diverse scenarios.

- XGBoost showcased the highest overall accuracy (around 86.4%) and the best F1 Score (approximately 0.58) among the three models.
- Random Forest followed closely, especially after hyperparameter tuning.
- Hyperparameter-tuned Logistic Regression showed improvement, but still lagged, particularly in terms of recall.
- Using SMOTE, models achieved a better balance between precision and recall, but at a slight cost to accuracy.
- Overall, model performance indicates that predicting customer exits is a complex task. There's a trade-off between different metrics to consider based on business needs.

## Conclusions and Recommendations

- In the initial models, the 'Complain' feature stood out, leading to a Random Forest accuracy of about 99.86% and XGBoost accuracy of about 99.83%. However, deeper analysis revealed an over-reliance on this feature, prompting further research and iterations without it. Further findings include:
- XGBoost with hyperparameter tuning appears to be the most promising model, striking a balance between accuracy and interpretability.
- SHAP indicated feature importance, suggesting that certain features predominantly influence predictions. Future strategies could focus on these features to mitigate churn.
- For businesses, grasping the factors leading to customer churn is paramount. While the models provide insights, qualitative research could offer deeper understandings of the underlying reasons.
- This project serves as a testament to the iterative and evolving nature of data science projects. Anomalies or dominant features like 'Complain' can sometimes lead to misleadingly high results. By identifying and addressing these issues, the project has paved the way for models that might have a broader application.

## Future Work

- Explore ensemble methods or neural networks for potentially better performance.
- Dive deeper into feature engineering to reveal more patterns.
- Continuously evaluate the model with new data to ensure robustness.
- Explore the combination of multiple models (ensembling) to enhance predictive capabilities.



## Contributing and Feedback

This research project is ongoing and for educational purposes.


