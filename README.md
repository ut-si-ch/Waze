# Waze
Classification of Waze data.

# Overview

The goal of this project was to develop a M.L. model to predict user churn. Churn quantifies the number of users who have uninstalled the waze app or stopped using the app. The project uses a synthetic data, called as waze_dataset.csv created in partnership with Waze. Logistic Regression, Random forest, and XGBoost models were used, among which Xg Boost performed well with accuracy of 81.8% and precision of 42.5%.

# Business Understanding
Waze faces the challenge of user churn, where user stop using or uninstalled the app, which is affecting the company's growth and user engagement levels. By developing a ML model to predict churn, waze can identify at risk users and understand why they leave. Solving this problem will help waze retain more users, improve the app experience, and ulimately support business growth by keeping its users base strong and active.

# Data Understanding

This project uses a dataset called waze_dataset.csv . It contains synthetic data created for this project in partnership with waze. The data consist of approximately 15k rows of unique users and 13 features. The features includes information about 'drives', 'driven_km_drives', ''activity_days', etc. The below pie-chart shows the number of retained vs churned users by percentage in the dataset.

![download](https://github.com/user-attachments/assets/814e3a7d-ee0e-4674-874d-dafe1796e952)

In connection to this new features were engineered and not useful features were dropped.

# Modelling and Evaluation
An XGBoost model was used to determine feature imortance to get an idea of which features are affecting the churn rate. The below plot shows the engineered features made up over half of the top 10 most predictive features used by the model. 

![download](https://github.com/user-attachments/assets/be0e9c8f-a662-4749-a9ab-4fae34b5f052)


The overall XGBoost model performed with 81.8% accuracy and 42.5 % precision. Intially Logistic Regresion was used which got an 82.3% accuracy and 51.7 % precision. But due to poor recall rate of 9.1% we shifted to Tree based models. Random Forest and XGBoost both models got better results than logistic regression. The recall score of XGBoost was nearly double the recall score of logistic regression and it's was almost 50% better than the random forest model's recalls score, while maintaining the similar accuracy and precision score.

# Conclusion
Recommeding this model for churn prediction  depends on what would the model be used for? If it is used to drive consequential business decisions then # NO , the model is not string enough predictor, as made clear by its poor recall score. However, if the model is only being used to guide further exploratory efforts, then it can have value. New features could be engineered like drive level information for each user suchas drive times, geographic locations. 
