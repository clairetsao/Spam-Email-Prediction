# Spam Email Prediction

Spam emails pose a significant challenge in the digital world, necessitating effective detection methods to safeguard users from unsolicited messages. This project focuses on predicting spam emails using a dataset obtained from the UCI Machine Learning Repository.

## Dataset

The dataset consists of 4601 records, each representing a different email message. Each record comprises 58 attributes, as described in the accompanying .names file. Attributes 1-57 denote various content-based characteristics extracted from each email message, such as word frequency, punctuation usage, and capitalization. The final attribute indicates the class label for each message, distinguishing between spam and non-spam emails.

Data: http://archive.ics.uci.edu/ml/datasets/Spambase 

## Predictive Models

Several machine learning algorithms, including Random Forest, KNN, SVM, Gradient Boosting, and XGBoost, are leveraged to construct predictive models. Hyperparameter tuning is executed using methodologies such as RandomizedSearchCV and GridSearchCV to optimize model efficacy. Two distinct models are developed based on varying criteria:

**Modeling (i): Best Accuracy**
This model prioritizes accuracy and is well-suited for general spam detection tasks.

**Modeling (ii): Best Cost-Sensitive**
Focused on minimizing misclassification costs, this model is tailored for scenarios where the financial ramifications of misclassifications are paramount.

## Model Evaluation

**Modeling (i): Best Accuracy**
The XGBoost model exhibits exceptional performance, achieving an accuracy of approximately 99.9% on the training set and maintaining a high accuracy of approximately 96% on the testing data. It excels in general spam detection tasks.

**Modeling (ii): Best Cost-Sensitive**
The Random Forest model emerges as the optimal choice for minimizing misclassification costs. Despite a slightly lower testing set accuracy of 94.06%, it effectively reduces misclassification costs, with a calculated cost of 262 and an average cost of 0.18. This model is valuable in scenarios prioritizing the financial impact of misclassifications.

Both models offer distinct advantages and can be selected based on the specific objectives and requirements of the spam email prediction task. While Modeling (i) emphasizes overall accuracy, Modeling (ii) addresses cost-sensitive performance, catering to diverse needs in spam email detection.
