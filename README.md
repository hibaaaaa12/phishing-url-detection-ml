# Phishing URL Detection using Machine Learning

## Objective
Build machine learning models to classify URLs as phishing or legitimate.

## Dataset
Kaggle phishing URLs dataset.

## Models Used
- Random Forest
- XGBoost

## Results

| Model         | Accuracy | Precision | Recall | F1 Score |
|---------------|----------|-----------|--------|----------|
| Random Forest | 94.65%   | 95.03%    | 94.30% | 94.67%   |
| XGBoost       | 91.22%   | 91.85%    | 90.60% | 91.22%   |

## Discussions
______________________________________________________________________________________________________________________________________________________________________________
1/Why Random Forest Performed Better
Random Forest outperformed XGBoost on this dataset (94.6% vs 91.2% accuracy).
This may be due to the dataset being relatively clean and balanced, where ensemble bagging methods like Random Forest perform strongly without heavy hyperparameter tuning.
XGBoost may require more tuning to surpass Random Forest performance.
______________________________________________________________________________________________________________________________________________________________________________
2/Dataset Balance Observation
The dataset is almost perfectly balanced (50.05% phishing, 49,990% legitimate).
The dataset appears artificially balanced and may not reflect real-world phishing distributions.
In real-world scenarios, phishing URLs represent a very small fraction of total URLs.
Therefore, performance metrics may be optimistic compared to real-world deployment conditions.
______________________________________________________________________________________________________________________________________________________________________________
## Limitations
- Dataset may not reflect real-world class imbalance
-XGBoost was manually configured with non-default hyperparameters:
  - n_estimators=300
  - learning_rate=0.05
  - max_depth=6
  - subsample=0.8
However, no systematic hyperparameter search (e.g., GridSearchCV) was performed.
- Model not tested on unseen external dataset


## Future Improvements
- Cross-validation
- Hyperparameter tuning
- ROC curve analysis
- Real-world imbalanced testing

## Author
Hiba Allah Bouazza
