# SAS e-Miner Documentation

## Overview
SAS e-Miner was used for data imputation to handle missing value, focusing on the construction of models such as decision trees, ensembled methods including Random Forest and Gradient Boosting.

## SAS flow

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/SAS%20Enterprise%20Miner/SAS%20flow.jpg)

### Specify Variable Roles
After the file has been imported in SAS Enterprise Miner, we have to specify variable roles first. The figure below shows the variable roles selection for your reference.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/SAS%20Enterprise%20Miner/Variable%20role.jpg)

## Impute

As I have used Talend Data Preparation to identify missing value for each column, so I only need to select the variables which are required for data imputation. As shown in below figure, you can see that I have imputed 7 variables to handle missing values.
-	Categorical type variables have been imputed by using method of tree to replace missing data with estimated or predicted values. Tree method ensures that datasets are complete and suitable for analysis. “Tree method” refers to decision tree-based method for imputing missing values. Decision tree will observe the relationship in the existing data to predict and fill in missing values.
-	For numerical type variables, mean imputation has been used to replace missing values with the mean (average) value of the observed data for the particular variable.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/SAS%20Enterprise%20Miner/Data%20Imputation.jpg)

## Model

### Decision Trees
**Construction:** Decision trees were built to understand patterns in the data. Different depth of Decision Trees have been built in SAS E-miner.

image
image
image
image


### Ensembled Methods
**Random Forest for Bagging**

**Gradient Boosting for Boosting**


## Model Comparison

image
