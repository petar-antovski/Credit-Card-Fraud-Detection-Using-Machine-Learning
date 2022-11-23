# Credit-Card-Fraud-Detection-Using-Machine-Learning

## Background

It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase

## Project Plan

    1. The dataset was obtained from Kaggle.

    2. The explored and engineered data was preprocessed.
        - The data was split into training and testing sets.
        - Both training and testing sets were checked for duplication and missing values were checked.
            - Missing numerical data was imputed using median.
        - Outliers were identified and cleaned.
        - Features were then scaled to map the variables onto the same scale.

    3. 12 baseline models were trained, including Logistic Regression, Decision Tree Classifier, K-Neighbors Classifier, MLP Classifier, Gaussian-Naive Bayes, Bernoulli-Naive Bayes, Multinomial Naive Bayes, Support Vector Classifier, SGD Classifier, Random Forest Classifier, Gradient Boosting Classifier and AdaBoost Classifier.
        - Nested cross validation was used to perform feature selection and hyperparameter tuning simulteneously, and then train the models, in order to mitigate overfitting.
        - SelectKBest was used for feature selection.
        - RandomizedSearchCV was used for hyperparameter tuning.
        - StratifiedKFold was used for cross validation as the dataset is highly imbalanced.
        - The models were evaluated based on Accuracy, Balanced Accuracy, Precision, Recall, F1 Score, ROC-AUC, PR-AUC, Cohen Kappa Score, Fit Time and Score Time.

    4.  The best performing models were shortlisted by focusing on the ‘Balanced Accuracy’, ‘F1’, ‘PR-AUC’, ‘ROC-AUC’, ‘Cohen's Kappa Score’ and ‘Time Taken For Training’ of the various models. These metrics were chosen as they are most suited for a highly imbalanced dataset.
        - Learning curves were also used to assess which models had overfitting.

    5. The 3 best performing models, were chosen for model stacking. 3 Ensemble Models were created using the combinations of these three classifiers.

    6. Lastly the 3 best performing models and the 3 Ensemble Models were evaluated using the same metrics as above and learning curves and the results were compare to determine the best model.

