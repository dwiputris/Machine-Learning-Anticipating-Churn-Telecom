# Machine-Learning-Anticipating-Churn-Telecom
With imbalanced observed data, a search for the best model is conducted. The telecommunications operator named Interconnect wants to predict the churn rate of their clients. If it is known that a client plans to terminate their service, they will be offered promotional codes and special package options.

The best model built in this project is one that uses Logistic Regression. Resizing-sample method was important to handle the imbalanced data where class 1 (Churn) was the minority. It is interesting that Logistic Regression came out with better result than XGBoost and Catboost Classifier in this project. Although the ROC-AUC level is better only by very slim difference, but considering its way more simplistic process, it is a significant finding.

The ROC-AUC score is 85.28, PR-AUC score is 66.51, and accuracy score is 76.12.

Recall of class 1 (Churn) is 80, and precision is 52.

The exploratory data analysis (EDA) and statistical analysis helped in finding the most relevant variables to churn, that is: type of contract, internet service pacakge subscribed, and monthly charges. It also led to decision on what additional features needed to be engineered. That in turn helped to add relevant variables even more, that is ratio of total charges to monthly charges, and average of monthly charges per type of subscription.

Non-existing data of customers in internet dataset and phone service dataset were very significant. When they first were treated as random missing values, no models could perform well enough. But when they were seen as customers not subscribing to particular services, models improved significantly.

Many additional, enginereed features were built, but some were dropped eventually. A variable 'duration' that is the period length of customer churn was built and it did make the model prediction 99% correct. But it caused a data leakage, hence was dropped from final model.

Catboost Classifier has proved to be resilient to the existence of irrelevant features. But removing them did improve performance of the model a Logistic Regression model significantly.

In conclusion, the model chosen is enough to predict churned customers of Interconnect where the recall rate enables the company to anticipate, and the precision is good enough to prevent from wasting too much valuable resources.
