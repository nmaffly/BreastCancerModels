# Comparing efficacy of different machine learning models to classify cases of breast cancer

## To Replicate
1. Download .ipynb file
2. Upload to notebook or colab
3. Run

## Important Metrics:
**Confusion Matrix:**

|              | Predicted Positive | Predicted Negative |
|--------------|---------------------|--------------------|
| **Actual Positive** | True Positive (TP) | False Negative (FN)|
| **Actual Negative** | False Positive (FP)| True Negative (TN) |


**Precision:** Tells us the accuracy of positive predictions
  - $\text{true positives} \over \text{true positives} + \text{false positives}$

  
**Recall:** Tells us how well the model identifies positive cases
  - $\text{true positives} \over \text{true positives} + \text{false negatives}$


**F1 Score:** A combination of precision and recall, ratio ranging from 0 to 1 (higher is better). Useful to look at when there is an uneven class distribution
  - $2 * {(Precision * Recall) \over (Precision + Recall)}$


**Accuracy:** a general indicator of how well the model is performing, but can be misleading when there is an uneven class distribution
  - $\text{correctly predicted cases} \over \text{total cases}$


**AUC Score:** Tells us how well the model is able to distinguish between positive and negative cases (for binary classification)


## Logistic Regression Model

A logistic model is good for categorizing numerical data where the relationship between independent variables and the log-odds of the binary outcome is assumed to be linear. 

Confusion matrix:
| 62 | 1  |
|----|----|
| **2**  | **106** |


Results from model:
- Precision: 0.98
- Recall: 0.98  
- F1 Score: 0.98
- Accuracy: 0.98
- AUC Score: 0.998


## K-Nearest Neighbors

K-Nearest Neighbors models pick values based on the data points that have the most similar feature values to the query point. Better to use over logistic regression when categorizing things like animals.

Confusion matrix:
| 59 | 4  |
|----|----|
| **3**  | **105** |


Results from model:
- Precision: 0.96
- Recall: 0.96  
- F1 Score: 0.96
- Accuracy: 0.96
- AUC Score: 0.977


## Support Vector Machine

This model categorizes data by splitting it with a line or hyperplane. It's good for high-dimensional data where there is clear margins of separation between classes. 

Confusion matrix:
| 61 | 2  |
|----|----|
| **3**  | **105** |


Results from model:
- Precision: 0.97
- Recall: 0.97  
- F1 Score: 0.97
- Accuracy: 0.97
- AUC Score: 0.996


## Decision Tree Classifier

Decision Tree Classifiers makes predictions by making decisions based on features in a tree-like structure. Each branch of tree represents the otucome of a decision and each leaf node represents the final prediction.

Confusion matrix:
| 60 | 3  |
|----|----|
| **7**  | **101** |


Results from model:
- Precision: 0.94
- Recall: 0.94  
- F1 Score: 0.94
- Accuracy: 0.94
- AUC Score: 0.944


## Random Forest Classifier

A Random Forest Classifier is a combination of multiple decision trees. They are good for handling complex relationships in data. They also reduce overfitting and increase model stability.

Confusion matrix:
| 61 | 2  |
|----|----|
| **3**  | **105** |


Results from model:
- Precision: 0.97
- Recall: 0.97  
- F1 Score: 0.97
- Accuracy: 0.97
- AUC Score: 0.996

## Gradient Boosting

This model starts with one tree and builds from scratch. It builds more trees sequentially and corrects errors of the previous ones. Analogy: solving a puzzle by asking a highschooler what to do for each step. Each high schooler is a "boost"

Confusion matrix:
| 59 | 4  |
|----|----|
| **3**  | **105** |


Results from model:
- Precision: 0.96
- Recall: 0.96  
- F1 Score: 0.96
- Accuracy: 0.96
- AUC Score: 0.996

## Naive Bayes

This model is based on the Bayes theorem, in which every single parameter is assumed to be completely independent (a 'naive' statement to make). Better for classification, not well-suited for regression tasks.

Confusion matrix:
| 57 | 6  |
|----|----|
| **5**  | **103** |


Results from model:
- Precision: 0.94
- Recall: 0.94  
- F1 Score: 0.94
- Accuracy: 0.94
- AUC Score: 0.993

## Neural Network

Neural networks are deep learning models (based on the human brain) composed of layers called neurons that contain data. The data is trained and analyzed, and the model back propogates and optomizes until it gets accurate results.

Confusion matrix:
| 61 | 2  |
|----|----|
| **2**  | **106** |


Results from model:
- Precision: 0.98
- Recall: 0.98  
- F1 Score: 0.98
- Accuracy: 0.98

## Adaboost Classifier

This model only focuses on what it got wrong, and strengthens itself in those areas. As a consequence, it doesn't get better in what it got right, which means it requires clean data to ensure the correct % is stable.

Confusion matrix:
| 61 | 2  |
|----|----|
| **2**  | **106** |


Results from model:
- Precision: 0.98
- Recall: 0.98  
- F1 Score: 0.98
- Accuracy: 0.98
- AUC Score: 0.996

## Extreme Gradient Boost

Similar to a gradient boost, but more faster and efficient. However, it is more complex and interpretable. Analogy: asking a professor instead of highschooler.

Confusion matrix:
| 61 | 2  |
|----|----|
| **3**  | **105** |


Results from model:
- Precision: 0.97
- Recall: 0.97  
- F1 Score: 0.97
- Accuracy: 0.97
- AUC Score: 0.994

## Visualizing the Models

### ROC Curves
Receiver Operating Characteristic (ROC) curves are used to assess the performance of a binary classification model. It plots the true positive rate (sensitivity) against the false positive rate (specificity). The diagonal line represents classification by random chance, and points above the line indicate that the model performs better than random guessing (50-50 chance). All models performed well, as indicated by the placement of all curves in the upper left corner.

![image](https://github.com/nmaffly/BreastCancerModels/assets/118420820/2d9c9a0a-5bda-4d2f-893e-1f4d32135c2d)

### Precision-Recall Curves
Precision-Recall Curves represent the relationship between precision and recall. Higher precision and recall values are more desirable, therefore curves that lie closer to the upper right corner are generally considered better. These curves are particularly useful when dealing with imbalanced datasets. 

![image](https://github.com/nmaffly/BreastCancerModels/assets/118420820/e5898b69-7434-439e-85d9-b17ae1fd52e6)




