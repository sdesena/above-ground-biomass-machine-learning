# Aboveground Biomass Prediction

## Overview

The prediction of aboveground biomass is essential for understanding ecosystems and the sustainable management of natural resources. This project aimed to develop predictive models using remote sensing data and machine learning techniques.

## Objectives

The primary objective of this work was to:

- Develop predictive models for aboveground biomass using remote sensing data.
- Employ machine learning techniques for enhanced accuracy and reliability.
- Map aboveground biomass at the study area.

## Methodology

The methodology included the following key components:

- **Sampling Techniques:** Methods for selecting representative data samples.
- **Cross-Validation:** Used to assess model performance and avoid overfitting.
- **Variable Selection:** Identification of relevant features for model training.
- **Hyperparameter Optimization:** Fine-tuning model parameters for improved accuracy.
- **Model Explanation with SHAP:** Interpreting model predictions to understand feature contributions.
- **Validation with NFI Data:** Comparing model predictions with data from the National Forest Inventory (NFI).

## Accuracy Assessment

Model performance was evaluated using metrics obtained through K-fold cross-validation, including:

- **Root Mean Square Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **Adjusted Coefficient of Determination (R²)**

### Results

- **Random Forest Model:** Adjusted R² = 62.7%
- **XGBoost Model:** Adjusted R² = 62.0%
- **Artificial Neural Network (DNN):** Adjusted R² = 60.4%

When comparing the predicted biomass with data obtained from NFI, a difference of -8.66 t/ha was identified, indicating that the Random Forest model's predictions are, on average, lower than the values measured directly in the field. 

Additionally, the Mann-Whitney U test found no statistically significant differences in performance metrics among the models.

## Contribution

This work contributes to the field of environmental management by providing a tool that can be used to support decision-making in conservation policies and the sustainable use of forest resources.
