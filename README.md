# Customer-Churn-Prediction-with-PySpark

This is a capstone project for [Udacity Data Science Nanodegree](https://www.udacity.com/course/data-scientist-nanodegree--nd025) 

#### -- Project Status: [Completed]

## Project Motivation

* to learn how to use AWS .
* handle large dataset using Spark.
* mimic real world scenario.


### Technologies
* Python
* PySpark
* SQL
* Pandas, numpy
* AWS
* matplotlib, seaborn

## Project Description
In this project, we will be creating a predictive model for customer churn prediction of a fictional music streaming service: Sparkify (similar to Spotify and Pandora). We first explore Sparkify usage data in tiny dataset (240mb) and find potential features for applying machine learning models. An appropriate metrics will then be selected to evaluate the machine learning models. Three models with default hyperparameters are used at first to compare the perforamce. We then perform hyperparameter tuning for the three models and pick the best model. Finally, we apply the tuned model in the full dataset and compare the difference in performance with the tiny dataset.   

Churn prediction is about making use of customer data to predict the likelihood of customers discontinuing their subscription in the future. Predicting churn rate is important because it can help Sparkify to identify and improve areas where customer services is lacking. So churn prediction helps to prevent individuals from discontinuing their subscription. According to [ClickZ](https://www.clickz.com/are-ecommerce-customer-retention-strategies-improving/105454/), the probability of selling to an existing customer is 60 - 70%. However, the probability of selling to a new prospect is just 5-20%.
So it is very important to keep the existing customer around. The [blog post](https://andrew-siu12.github.io/2019-09-04-Customer-Churn-Prediction-with-PySpark/) provides detailed explanation of the project.

### Data
There are two dataset made avaliable, a full dataset (12GB) and a tiny subset (240Mb) sample from the full dataset. We will use the subset for data exploration, feature engineering and model selection on local machine. Its more time and computationally efficient to do all the modelling work in a small dataset than working on full dataset. If the subset of data is indeed representative of the full dataset, feature engineering and hyperparameters tuned in the sample dataset should applicable to the full dataset.


## Needs of this project

- data exploration/descriptive statistics
- data processing/cleaning
- machine learning
- hyperparameter tuning
- writeup/reporting

## File Descriptions
```
├─images
└─notebook
        Sparkify.html
        Sparkify.ipynb
        SparkifyAWS.html
        SparkifyAWS.ipynb
```
1. Sparkify.html: html file of the data analysis for customer churn prediction for Sparkify in small dataset
2. Sparkify.ipynb: jupyter notebook of the analysis and modelling
3. SparkifyAWS.html:  html file of the data analysis and modeling of full dataset in AWS EMR cluster
4. SparkifyAWS.ipynb: jupyter notebook of the data analysis and modeling of full dataset in AWS EMR cluster

## Summary

In this project, i first cleaned the missing values of the data by removing rows with no userId, and assign None to missing values of artist, song and 0 to feature length. We then perform some analysis to find out the relationship of churn rate with different features. For feature engineering, we crafted 18 features based on the analysis and common sense. We selected 3 models for prediction, namely logistic regression, random forest and gradient boosting tree classifier. The result of hyperparameter tuning shows that random forest classifier have the best overall performance with less computational time and better score than the other two classifiers. Finally, we use the hyperparameter tuned in the small dataset to train on the full dataset. The result is summarized in following table:

| Dataset      | accuracy | precision| recall | f1 score| 
| -------------   |:--------:| --------:| ------:| -------:|
| 240mb dataset | 0.89655|  0.89533|0.89655|0.88623|
| Full 12Gb dataset | 0.84919|  0.85287|0.84919|0.8272| 

A summary post has been written on my own [blog] (https://andrew-siu12.github.io/2019-09-04-Customer-Churn-Prediction-with-PySpark/)

