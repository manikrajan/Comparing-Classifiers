# Comparing-Classifiers

# Overview

This repo explores the dataset from the UCI Machine Learning repository. The data is from a Portuguese banking institution and is a collection of the results of multiple marketing campaigns. The original dataset contained information on 3 million used cars. The dataset in this repo contains 41188 observations and 20 features from 17 marketing compaigns completed by the bank to influence their clients to subscribe to term deposits.  The goal is to predict if the client will subscribe a term deposit.  

# Business Understanding

This task aims to develp a Machine learning model to predict if the client will subscribe a term deposit based on the data provided. In this task, k-nearest neighbors, logistic regression, decision trees, and support vector machines models will be developed to identify the best performing model and to identify key features that influence the clients. The models developed will provide insights into the patterns and relationship in the data

# Data Understanding & Preparation

- No missing data
- Only 10% of the clients subscribed by the end of the compaigns
- Proportion of people less than 20 years old and age more than 60 years old has higher subscription rate
- Quarter end sees more subscriptions
- No correlation between the number of compaigns in each month and the subscription rate 

# Modeling

  Built the following  linear regression models.
  - Baseline model produced a accuracy of about 88.65%
  - Build simple logistic regression,KNN,Decison tree and SVM models
  - All models produced an accuracy close to the baseline model.
  - It indicates the models needs tuning
    
![image](https://github.com/manikrajan/Comparing-Classifiers/assets/6862254/9733cfca-a181-4e07-b999-6a9877241dc5)

 
# Evaluation
- After tuning the models with GridSearchCV and relevant hyperparameters, Decision tree and KNN performed better compared to other models with 90% and 89.4% accuracy respectively. KNN fit time was faster(0.48s) 
- Logistic regression with quadratic features took a long time(~44008s) to fit with a test accuracy of 86.2%
- SVM was extremely slow to fit even after reducing the features using PCA. The accuracy was ar 89.7% .The best kernel was "RBF'
- Education, Age, Marital status, Job and Default are the influencing features
