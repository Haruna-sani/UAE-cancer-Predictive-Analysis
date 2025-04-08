# README: Cancer Patient Classification Models (UAE)

## Overview
This repository contains machine learning models designed to classify cancer patients in the UAE into one of three categories:
- **Recovered**
- **Under Treatment**
- **Deceased**

The dataset used for training and testing the models consists of medical data from cancer patients. To address the issue of data imbalance, **SMOTE** (Synthetic Minority Over-sampling Technique) was employed. The models in this study include **XGBoost**, **Random Forest (RF)**, **Artificial Neural Network (ANN)**, and a hybrid model combining **ANN + RF**. Cross-validation with 10 folds was used to optimize the parameters of the models.

## Models Used

### 1. **XGBoost**
- **Accuracy**: 0.4485
- **Recall**: 0.3256

### 2. **Random Forest (RF)**
- **Accuracy**: 0.3650
- **Recall**: 0.3199

### 3. **Artificial Neural Network (ANN)**
- **Accuracy**: 0.4870
- **Recall**: 0.1623

### 4. **ANN + RF Hybrid Model**
- **Accuracy**: 0.3320
- **Recall**: 0.3386

## Best Model Selection
After evaluating the models based on their **accuracy** and **recall**, the **ANN** model with an accuracy of **0.4870** achieved the highest accuracy. However, the **ANN + RF** hybrid model showed the highest recall of **0.3386**, indicating a better ability to identify the positive class in the imbalanced dataset.

In this case, the **ANN model** is selected as the best model for classifying cancer patients due to its higher accuracy, even though the hybrid model shows improved recall.

### Data Preprocessing
- **SMOTE** is applied to handle data imbalance.
- The dataset is split into features and labels, with preprocessing steps applied to scale the data.

### Model Training
The following models are trained with 10-fold cross-validation:

- **XGBoost**
- **Random Forest**
- **Artificial Neural Network (ANN)**
- **ANN + RF Hybrid Model**

### Model Evaluation
Each model is evaluated based on:
- **Accuracy**: Measures the proportion of correctly classified instances.
- **Recall**: Measures the proportion of actual positives that were correctly identified.



## Results Summary

| Model        | Accuracy | Recall   |
|--------------|----------|----------|
| **XGBoost**  | 0.4485   | 0.3256   |
| **RF**       | 0.3650   | 0.3199   |
| **ANN**      | 0.4870   | 0.1623   |
| **ANN + RF** | 0.3320   | 0.3386   |

## Conclusion
Based on the evaluation metrics, the **ANN model** with the highest accuracy of **0.4870** is considered the best model for classifying cancer patients in the UAE. Despite the lower recall, the **ANN model** is more effective at predicting the correct classes with higher accuracy. The **ANN + RF hybrid model** has the highest recall, which may be useful for some applications where identifying all true positive cases is more important than overall accuracy.

