# TelcoChurn

# Customer Churn Prediction

![pic](./data/teleco.jpg)

## Table of Contents
1. [Introduction](#introduction)
2. [Methodology](#methodology)
    1. [Exploratory Data Analysis (EDA)](#eda)
    2. [Predictive Modeling](#predictive-modeling)
3. [Conclusion](#conclusion)

## 1. Introduction
In today's highly competitive telecommunications industry, retaining customers is a top priority for businesses. Customer churn can significantly impact a company's revenue and market share. Leveraging data and machine learning techniques can provide valuable insights into predicting and addressing churn effectively.

This project focuses on churn prediction using a telecom dataset. We will start by conducting an in-depth exploratory data analysis (EDA) to gain insights into the key factors influencing customer churn. Subsequently, we will apply various machine learning models, including logistic regression, XGBoosting and glmnet for predictive analysis. Our goal is to equip telecom companies with actionable insights and predictive tools to help them reduce churn and enhance customer retention.

You will find detailed code and analysis, in the Jupyter notebook named "ChurnPred" as well as the Rmd "GLMNET" which explains the glmnet model donde in R.
For each of the Machine Learning models we have applied different data preprocessing techniques to adjust the data depending on the model and it´s characteristics.

## 2. Methodology
### 2.1. Exploratory Data Analysis (EDA) <a name="eda"></a>
In the exploratory data analysis (EDA), we delved into the characteristics of numeric columns, highlighting aspects such as distribution and key statistics. We observed clear asymmetry in the numeric variables, and through the correlation matrix, we identified significant relationships between the probability of churn and various key variables, such as customer tenure and total charges. Addressing the class imbalance challenge in our dataset, where 73.46% are labeled as "no churn" and 26.54% as "churn," we chose not to apply oversampling techniques to avoid potential biases. 

### 2.2. Predictive Modeling <a name="predictive-modeling"></a>

Three primary models will be explored in this notebook:

1. **Logistic Regression:** Logistic regression is a fundamental machine learning algorithm used for binary classification problems. The logistic regression process involves data preparation, where variables are categorized and encoded, and training the model using cross-validation with a focus on ROC-AUC metrics. To optimize the model's performance, the classification threshold is adjusted manually, emphasizing a balance between correctly identifying churners and resource allocation.

2. **XGBoosting:** The XGBoosting model, a pivotal component in our churn prediction algorithm, employs decision tree ensembles to enhance predictive accuracy. Through meticulous data preprocessing, including numerical and categorical handling, the model identifies influential features like total customer service requests and contract type. Trained and evaluated on a stratified dataset, the XGBoost model consistently achieves a recall score of 0.8024 through K-fold cross-validation. The ROC curve further demonstrates its effectiveness in distinguishing true positives and false positives across different thresholds, affirming its robust predictive capabilities.

3. **GLMNET Model (R):** The GLMNET model will be implemented in R, and its code and evaluation will be provided in a separate readme.GLMNET, short for Generalized Linear Model Elastic-NET, incorporates Elastic-Net regularization, merging Lasso and Ridge methods. Ridge minimizes coefficients' squares with a regularization parameter λ, while Lasso can force some coefficients to precisely zero, highlighting essential features. Elastic-Net combines both, introducing an α variable to control the Ridge-Lasso balance. Top Lasso coefficients reveal influential predictors. Cross-validation determines optimal λ values, showcasing a trade-off between model complexity and predictive power. The ROC curve illustrates a 0.027 improvement in ROC-AUC compared to regular logistic regression, showcasing GLMNET's enhanced predictive performance.

## Conclusion <a name="conclusion"></a>

The telecommunications industry faces a constant challenge to retain customers in a highly competitive market. Predictive models and data-driven strategies are instrumental in identifying potential churners and implementing tailored retention initiatives. This project demonstrates the effectiveness of logistic regression and XGBoosting in predicting customer churn.

Through the methodologies presented, telecom companies can gain valuable insights into customer behavior and take proactive measures to reduce churn rates. We believe this analysis can be a stepping stone towards enhancing customer loyalty and business sustainability in the telecom sector.


_**Note:** The code for this project can be found in the "churn_pred" Jupyter notebook and GLMNET.Rmd._

Feel free to explore the code and analyses in the notebook for a deeper understanding of the project.