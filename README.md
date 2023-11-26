# Parkinson-Disease-Prediction

### Introduction

Speech disorders can significantly impact communication and overall quality of life. Early detection and intervention are crucial for improving outcomes. In this project, we explore the use of machine learning to classify speech features and identify potential speech disorders.

### Data Preprocessing

The dataset comprises 756 individuals' speech features and corresponding labels indicating the presence or absence of a speech disorder. To enhance model performance, we employed data preprocessing techniques.

#### Data Cleaning

Redundant or highly correlated features can hinder model performance. We removed features with correlation coefficients exceeding 0.7, resulting in a reduced dataset with 252 rows and 287 columns.

#### Feature Selection

To further refine the dataset, we applied the chi-squared test along with SelectKBest. This approach identified 30 features with significant correlation to the target variable, reducing the dataset to 252 rows and 31 columns.

#### Data Balancing

The dataset exhibited an imbalance in target class distribution. To address this imbalance, we employed RandomOverSampler, oversampling the minority class (speech disorder) to match the majority class (no speech disorder).

### Model Training and Evaluation

We trained and evaluated three machine learning models: Logistic Regression, XGBClassifier, and SVC. Each model was assessed using training and validation datasets.

#### Logistic Regression

Logistic Regression demonstrated superior performance, achieving a training accuracy of 83.06% and a validation accuracy of 81.27%.

#### XGBClassifier

XGBClassifier attained a training accuracy of 99.99% but a lower validation accuracy of 78.57%, indicating potential overfitting.

#### SVC

SVC achieved a training accuracy of 71.05% and a validation accuracy of 75.87%.

### Conclusion

Logistic Regression emerged as the most effective model for predicting speech disorder based on speech features. It demonstrated a balance between training and validation accuracy, indicating its ability to generalize well to unseen data.

### Beyond Accuracy: Understanding Model Behavior

To gain deeper insights into the model's decision-making process, we visualized the confusion matrix, revealing an 83% accuracy in identifying individuals with a speech disorder.

#### Confusion Matrix

The confusion matrix depicts the actual versus predicted classes:

```
[[10  4]
 [ 2 35]]
```

True positives (correctly identified speech disorder): 10
False negatives (speech disorder misclassified as no speech disorder): 2

True negatives (correctly identified no speech disorder): 35
False positives (no speech disorder misclassified as speech disorder): 4

### Empowering Early Detection

The project demonstrates the potential of machine learning in classifying speech features and identifying potential speech disorders. Early detection can facilitate timely intervention and improve outcomes for individuals affected by speech disorders.

### Future Directions

Future research could explore the use of deeper learning models and investigate the impact of additional speech features on model performance. Additionally, incorporating multimodal data, such as auditory and visual features, could further enhance the predictive capabilities of speech disorder detection systems.
