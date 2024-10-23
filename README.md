# Aboveground Biomass Prediction

## Overview

The prediction of aboveground biomass is essential for understanding ecosystems and the sustainable management of natural resources. However, field data collection faces cost and feasibility limitations when applied on a large scale, making accurate biomass mapping challenging. As an alternative, remote sensing, combined with machine learning techniques, has proven to be an scalable and effective tool for estimating biomass in large areas, with greater precision and lower cost.

The workflow on this project utilizes a combination of diverse datasets. First of all is MapBiomas (collection 7) to make a Land Use and Land Cover analysis on the area of interest. Then, the target variable is sampled using ESA CCI Global Forest Above Ground Biomass. The Harmonized Sentinel-2 MSI (Level-2A) and Sentinel-1 SAR GRD with log scaling were used to get vegetation indices, biophysical parameters and texture measures as features. The features also incorporates NASA SRTM Digital Elevation (30m) and ETH Global Sentinel-2 10m Canopy Height (2020), contributing to a robust and detailed approach.

## Objectives

The primary objective of this work was to:

- Develop and implement predictive models for aboveground biomass using remote sensing data.
- Assess the accuracy of these models and compare it with National Forest Inventory (NFI) data.
- Generate reliable maps of aboveground biomass for the study area.

## Methodology

The methodology included the following key components:

- **Sampling Techniques:** Methods for selecting representative data samples such as grid and random sampling.
- **K-Fold Cross-Validation:** Used to assess model performance and avoid overfitting.
- **Variable Selection:** Identification of relevant features for model training with Mean Decrease in Accuracy (MDA) and Mean Decrease in Impurity (MDI).
- **Hyperparameter Optimization:** Fine-tuning model parameters with Bayesian and Random Search for improved accuracy 
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
