# Telecom Churn Case Study

## Problem Statement

## Business Problem Overview

In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business goal.

To reduce customer churn, telecom companies need to predict which customers are at high risk of churn.

In this project, we will analyse customer-level data of a leading telecom firm, build predictive models to identify customers at high risk of churn and identify the main indicators of churn.

We used the CRISP framework for building the model. We did following steps
- ***1. Business Issue Understanding***
- ***2. Data Understanding***
- ***3. Data Preperation***
- ***4. Building the Model***
- ***5. Validating the model***
- ***6. Presenting the findings***

During the building of model we tried with different models
1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Random Forest with PCA
5. K Nearest Neighbour Classifier
6. XGB Classifier

We got the following results

| Model | Train Score | Test Score |
| --- | --- | --- |
| Logistic Regression | 0.93 | 0.93 |
| Decision Tree | 1.0 | 0.91 |
| Random Forest | 1.0 | 0.94 |
| Random Forest With PCA | 1.0 | 0.92 |
| K Nearest Neighbour| 0.93 | 0.91 |
| XGB | 0.98 | 0.94 |

We see that the best results were given by Random forest and XGB

We also tried GridSearch on top of both of the above which improved the accuracy slightly

We finally used the GridSearch on XGB classidier and found the below best parameters

Best Parameters: {'colsample_bytree': 0.7, 'gamma': 0.1, 'learning_rate': 0.1, 'max_depth': 5, 'n_estimators': 100, 'subsample': 0.5}
Accuracy: 0.9416666666666667

This model was used for prediction and we have attached the reuslts. But since Gridsearch requires very heavy resources we have commented the gridsearch code. 

We have included the normal XGB classifier code in the sheet
