# Bike-Rental-Prediction-with-Interaction-Effects
# Bike Rental Prediction with Interaction Effects

This repository contains an analysis of bike rental predictions using linear regression models, with and without interaction effects. The goal is to assess how incorporating interactions between different features can improve the model's ability to predict rented bike counts. The dataset includes various features such as temperature, humidity, season, and other environmental factors.

## Overview

The main objective of this project is to:

- Predict the number of rented bikes using multiple features.
- Explore the impact of interaction effects between features on the predictive performance of the model.
- Compare the performance of models with interaction terms versus those without interaction terms.

## Features

The following interaction pairs were considered for the analysis:

1. **Temperature * Humidity** (both numerical)
2. **Seasons_Spring * Wind_speed** (categorical and numerical)
3. **Seasons_Summer * Visibility** (categorical and numerical)
4. **Seasons_Winter * Dew_point_temperature** (categorical and numerical)

### Steps Taken

1. **Data Preprocessing**:
   - Target variable (rented bike counts) was log-transformed to address skewness.
   - Interaction features were created using `PolynomialFeatures` with the `interaction_only=True` parameter.

2. **Model Building**:
   - Linear regression models were built both with and without interaction effects for each pair of features.
   - The R² (coefficient of determination) was calculated to assess model fit and compare the two types of models.

3. **Evaluation**:
   - Models were evaluated on the test dataset, and performance was compared using the R² metric.

## Results

The inclusion of interaction effects significantly improved the **R²** values for all the models compared to those without interaction effects. The results are summarized below:

| Interaction Pair                                      | R² without Interaction | R² with Interaction |
|-------------------------------------------------------|------------------------|---------------------|
| Temperature * Humidity                                | 0.58                   | 0.75                |
| Seasons_Spring * Wind_speed                           | 0.64                   | 0.72                |
| Seasons_Summer * Visibility                           | 0.60                   | 0.74                |
| Seasons_Winter * Dew_point_temperature                | 0.62                   | 0.76                |

## Installation

To run the project, clone this repository to your local machine:

```bash
git clone https://github.com/your-username/Bike-Rental-Prediction-with-Interaction-Effects.git
cd Bike-Rental-Prediction-with-Interaction-Effects
