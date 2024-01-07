## Result and Analysis

### Decision Tree Analysis

After constructing decision tree, we use “Model Comparison” to evaluate performance among these 4 models. The result is showed as below.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Result%20%26%20Analysis/decisiontreeresult.jpg)

Models like Decision Tree - Maximal seem to generalize well, showing low misclassification rates on both training and validation sets. However, the decision trees like lvl 2, lvl 3 and lvl 4 exhibit signs of overfitting, especially as the misclassification rates increase on the training set compared to the validation set. Overfitting may lead to poor generalization and inaccurate predictions on new data while underfitting may result in a model that is too simplistic and fails to capture important patterns in the data as well. Hence, boosting and bagging techniques will be explored in next section.

As compared to model performance, the misclassification rates generally decrease as the tree depth increases, indicating a trend of improved model performance with more complex trees. Decision trees at maximal level consistently outperforms Decision trees at various levels on both training and validation datasets.

Based on the decision tree developed, I found several interesting points in Decision Tree – Maximal. The variable importance for decision tree is acquired as below. It is found that 5 variables that have highest importance are **Tenure, Number of Address, Complain, Satisfaction Score and Cashback Amount** with importance 1.0, 0.5373, 0.5095, 0.3598 and 0.3456 respectively.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Result%20%26%20Analysis/variableimportance_DT.jpg)


### Ensemble Methods

Bagging and Boosting methods will be used to overcome overfitting / underfitting issues.

**1. Boosting Method**

Gradient Boosting has been used to handle the overfitting issues that are happened in Decision Tree – lvl 2, 3, and 4. Gradient Boosting builds a tree sequentially, where each tree corrects the errors of the previous one. Gradient Boosting includes regularization parameters like learning rate and tree depth to control the complexity of the model. The gradient boosting has been trained and compared with previous models. As you can see in below, the misclassification rate of gradient boosting is lower than compared to Decision Tree at level 2, 3, and 4, with the value of 0.1145 for training and 0.109403 for validation. Lower misclassification rates indicate improved model performance in term of accuracy, suggesting overfitting was gradually reduced. The results indicate that Gradient Boosting is a favourable model for the given task, outperforming individual Decision Trees.

**Result of Gradient Boosting**
![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Result%20%26%20Analysis/result_GB.jpg)

**Model Comparison Between Gradient Boosting and Decision Trees at various levels**

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Result%20%26%20Analysis/compare_DT_GB.jpg)

For the variable importance, we can also see there is slightly difference between decision tree and gradient boosting. I found out the variables such as **Tenure, Complain, Number of Address** are important in both models (Decision Tree and Gradient Boosting). Let’s explore bagging method to see whether the prediction will further improve or not.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Result%20%26%20Analysis/variableimportant_GB.jpg)

**2. Bagging Method**

For underfitting issue, we try to use bagging method, which is random forest to handle this issue. Random forest builds an ensemble of decision trees, and each tree is constructed independently, making them diverse. It introduces randomness by selecting a random subset of features at each split during tree construction. This randomness helps prevent individual trees from becoming too specialised. Random forest has been employed, as you see result below, random forest has a lower misclassification rate compared to Decision Tree at all levels, indicating better performance on the training data.

![Updated Image](https://github.com/sokqi918/WQD7005_AA1/blob/main/Result%20%26%20Analysis/result_overall.jpg)

Overall, random forest and gradient boosting consistently outperformed Decision Trees at various levels on both training and validation datasets. They exhibit lower misclassification rates and average squared errors, indicating better predictive performance. Among the models, Random Forest tends to have the lowest misclassification rates on both training and validation data, making it the top performer in this comparison. Indeed, decision tree is still a superior model, as we can see that the decision tree at maximal level is performed well which having the second lowest misclassification rate among the models on both training and validation datasets. This indicates that if we construct the decision tree well, it can be one of the superior models for classification and prediction. It's essential to consider the context of our analysis and the specific requirements of the task when choosing the most suitable model.


