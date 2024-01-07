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

### Result
The imputed variable results are fixed after we run the “impute”, the number of missing for TRAIN is aligned with the identified missing values in Talend Data Preparation.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/SAS%20Enterprise%20Miner/Data%20Imputation%20result.jpg)

## Model

### Data Partition
I have split the dataset to 70% of training set and 30% of validation set. For the rest properties, I put them as default setting.

Image

### Decision Trees

For decision tree construction, the ordinal target criterion has been set as “Entropy”.

Image

The rest of properties have been set as default setting; I only adjust the model settings to enhance its predictive power. Specifically, in this segment, I utilized the "interactive" feature to train the decision tree at various levels by adjusting the tree's depth.

Image


As mentioned earlier, I used ordinal target criterion as “Entropy”. In this case, the node will be split based on the entropy. In the context of decision trees and entropy, the goal is to minimize entropy. The entropy is a measure of impurity or disorder within a set of data, and decision trees seek to create splits that result in subsets with lower entropy. 

**Construction:** Decision trees were built to understand patterns in the data. Different depth of Decision Trees have been built in SAS E-miner.

**Decision Tree - lvl 2**


**Decision Tree - lvl 3**


**Decision Tree - lvl 4**

**Decision Tree - Maximal**


### Ensembled Methods
**Random Forest for Bagging**

**Gradient Boosting for Boosting**


## Model Comparison

image
