
# Model Card: Waist Measurement Prediction Models

This model card summarizes the development and evaluation of four machine learning models trained to predict waist circumference using anthropometric features.

---

## Model Description

**Inputs**:  
- Features used for prediction (in inches):
  - ShoulderWidth
  - ChestWidth
  - Belly
  - Hips
  - ArmLength
  - ShoulderToWaist
  - WaistToKnee
  - LegLength
  - TotalHeight

**Output**:  
- Predicted waist circumference (in inches), a continuous numerical value.

**Model Architectures**:
- **Random Forest Regressor**: Ensemble method based on multiple decision trees (100 estimators).
- **Linear Regression**: Classical linear model assuming a linear relationship between features and target.
- **Support Vector Regressor (SVR)**: Kernel-based model using the RBF kernel for non-linear regression.
- **Decision Tree Regressor**: Single decision tree model using recursive splitting based on feature thresholds.

---

## Performance

All models were evaluated using the following metrics:
- **MSE (Mean Squared Error)**
- **MAE (Mean Absolute Error)**
- **R² Score (Test Set Accuracy)**
- **Cross-Validated R² Score (5-Fold)**
  
Expected performance:

| Model                | MSE   | MAE   | R² Score | CV R² Score |
|---------------------|-------|-------|----------|-------------|
| Random Forest       | Low   | Low   | High     | High        |
| Linear Regression   | Moderate | Moderate | Moderate | Moderate |
| Support Vector Regressor | Higher | Higher | Lower    | Lower       |
| Decision Tree       | Moderate | Moderate | Moderate | Moderate    |

(Actual metric values were printed in code output)



---

## Limitations

- **Dataset Size**: Limited to 716 individuals (bootstrapped to ~1074), which may not generalize across global populations.
- **Synthetic Data Used**: Limited to 1000 synthesized individuals - using the CTGAN (Conditional Tabular GAN) model from the SDV library, which may not generalize across global populations.
- **Demographic Bias**: No demographic information such as ethnicity or geographic distribution was available.
- **Input Assumptions**: Assumes all features are available and measured accurately for prediction.

---

## Trade-offs

- **Random Forest**:
  - **Pros**: High accuracy, robust to noise and overfitting.
  - **Cons**: Slower to train and harder to interpret.

- **Linear Regression**:
  - **Pros**: Simple and interpretable.
  - **Cons**: Assumes linearity; underperforms with non-linear relationships.

- **Support Vector Regressor**:
  - **Pros**: Handles non-linear data using RBF kernel.
  - **Cons**: Sensitive to feature scaling; slower with large datasets.

- **Decision Tree**:
  - **Pros**: Easy to visualize and interpret.
  - **Cons**: Prone to overfitting, especially on small datasets.

---

**Author**: Grant Van Wyk  
**Date**: 17/06/2025
**Source Data**: Kaggle - Body Measurements Dataset (Saurabh Shahane)

