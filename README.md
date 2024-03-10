# H1N1-seasonal-flu-vaccines-prediction
![example](images/black_and_white_picture.jpg)
# Overview
The goal of this project is to create a predictive model for the likelihood of persons receiving seasonal flu vaccinations. We hope to understand the key determinants driving vaccine uptake and find solutions to boost immunization rates by using machine learning techniques and examining numerous socio-demographic and behavioral characteristics.
# Business Problem
The **National Vaccination Advisory committee** under the Government's Public Health Office aims to provide vaccination to the whole country and prevent the spread of seasonal flu and H1N1 flu. However, The National Vaccination Advisory faces a challenge on how to administer the vaccine since it isn't compulsory yet it is vital at the same time. Based on the previous vaccination campaigns, the government has had a tough time of deciding which group of citizens are likely to turn up for a vaccination and which are not. Moving forward, National Vaccination Advisory committee wishes to understand which factors contribute to a voluntary intake of the vaccine by the public given a warning of a flu and which factors do not. This information is beneficial to the National Vaccination Advisory committee as it would make it easier for them to identify and direct the necessary resources towards vaccination campaigns, awarness, disease mitigation and procurement procedures.
# Data Understanding
The data used in this project is from the **National 2009 H1N1 Flu Survey** collected to monitor vaccination rates during the US government vaccination campaigns. The survey asked people whether they had received H1N1 and seasonal flu vaccines. In the survey questions ranging from personal,social, economic to demographic and opinion questions among others were asked in order to have a better understanding of how these characteristics are associated with personal vaccination patterns and how the National Vaccination Advisory committee can provide guidance for future public health efforts.

This notebook contains three datasets namely:

1. training_set_features.csv = contains citizens information on their vaccine awarness, personal information, behavioral information and their opinions on vaccination.

2. training_set_labels.cs = contains information on whether a particular citizen was vaccinated or not.

3. test_set_features.csv = contains citizens information as well, but it will be used to test how well our model predicts new data

The training_set_features.csv contains 26707 Rows and 35 columns training_set_labels.cs contains information whether a respondent was vaccinated or not. (0) for No and (1) for yes
# Project Structure:

- Data: Contains the dataset used in the project. The data was collected by the National 2009 H1N1 Flu Survey to monitor vaccination rates during the US government vaccination campaigns. The data can be otabined at this link: https://www.drivendata.org/competitions/66/flu-shot-learning/


- Notebook: This folder contains the Jupyter notebook detailing the data preprocessing, exploratory data analysis (EDA), and modeling steps undertaken in the project.

- Models: Includes saved model files (.pkl) of the trained machine learning models for predicting vaccine uptake. (Still in progress). To see the models visit the Vaccine Prediction.ipynb

- Presentation: Contains the presentation slides summarizing the project findings, recommendations, and conclusions.

- Images: Contains image files which are used to beautify the readme header.

- README.md: You are here! This file provides a concise summary of the project, direction to the presentation and data sources, and instructions for navigating the repository.
# Approach

* Data Preprocessing: Cleaned and prepared the dataset by handling missing values, encoding categorical variables, and scaling numerical features.

* Exploratory Data Analysis (EDA): Conducted exploratory analysis to gain insights into the distribution of variables, identify patterns, and explore correlations between features and vaccine uptake.

* Modeling: Developed machine learning models, including logistic regression, random forest, and gradient boosting, to predict vaccine uptake based on the available features. Evaluated model performance using metrics such as accuracy, ROC AUC, F1 score, and recall.

# Models used in this project

1. Linear Regression
* Purpose: Used logistic regression to predict the likelihood of individuals getting the seasonal flu vaccine.
* Hyperparameter Tuning: Fine-tuned hyperparameters such as regularization strength, penalty, and solver using grid search.
* Performance: Achieved a test accuracy of 78.27% and an ROC AUC score of 0.78.

2. Random Forest
* Purpose: Used logistic regression to predict the likelihood of individuals getting the seasonal flu vaccine.
* Hyperparameter Tuning: Fine-tuned hyperparameters such as regularization strength, penalty, and solver using grid search.
* Performance: Achieved a test accuracy of 78.27% and an ROC AUC score of 0.78.

3. Feature Importance Analysis
* Identified important features influencing vaccine uptake using the GBM model.
* Top features included respondents' concerns about seasonal flu, knowledge about H1N1 and seasonal flu, and recommendations from doctors for both H1N1 and seasonal flu vaccines

4. Model Evaluation
* Evaluated models using performance metrics such as accuracy, ROC AUC, F1 score, and recall to assess predictive capability and generalization ability.
* Identified GBM as the preferred model due to its balanced performance and reduced overfitting compared to Random Forest.

# Conclusion
We experimented with three different types of models: Logistic Regression, Random Forest, and Gradient Boosting Machine (GBM). For each model, we performed hyperparameter tuning using grid search to optimize model performance.

The logistic regression model provided a solid baseline, achieving an accuracy of approximately 78% on the test set. However, it exhibited signs of bias towards predicting individuals who are less likely to get vaccinated, which could lead to higher false negative rates.

Next, we explored ensemble methods like Random Forest and GBM. Random Forest improved upon the logistic regression model, achieving a test accuracy of approximately 78% after hyperparameter tuning. However, it still suffered from some overfitting.

To address overfitting, we employed Gradient Boosting Machine (GBM). The GBM model demonstrated improved generalization performance, with training and testing accuracies converging closer together. It achieved a test accuracy of approximately 79%, along with good precision, recall, and F1 score metrics.

In conclusion, the GBM model is the most suitable model for predicting seasonal flu vaccine uptake and providing valuable insights for healthcare practitioners and policymakers.





