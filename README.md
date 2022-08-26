# Home Credit Default Risk

## Introduction

Kaggle is a web platform and community for data scientist and machine learning engineers where competetitions and datasets are regularly published.

This particular [competition](https://www.kaggle.com/c/home-credit-default-risk) is a binary Classification task: we want to predict whether the person applying for a home credit will be able to repay its debt or not.

The dataset is composed of multiple files with different information about loands taken. In this project we're going to exclusively work with the main files: application_train.csv and application_test.csv.

The competition uses [Area Under the ROC Curve](https://developers.google.com/machine-learning/crash-course/classification/roc-and-auc?hl=es_419) as the evaluation metric, so our models will have to return the probabilities that a loan is not paid for each row.

This particular competition is a binary Classification task: we want to predict whether the person applying for a home credit will be able to repay its debt or not.

In the notebook file, the following sections can be found:

## Data Exploration

A qualitative analysis of the data is done.

## Preprocessing

In this section, a function to make all the data pre processing for the dataset is implemented.

The function performs these activities:

- Correct outliers/anomalous values in numerical columns
- Impute values for all columns with missing data (using median as imputing value)
- Encode categorical features:
    - If feature has 2 categories encoding using binary encoding
    - More than 2 categories, using one hot encoding 
- Feature scaling

## Training Models

A LogisticRegression is used as a Baseline. Then a RandomForestClassifier with RandomizedSearchCV is used. Finally a LightGBM is used. 

## Using Scikit Learn Pipelines

As a final step, a Pipelines from Scikit learn was implemented to automate all the process. 
