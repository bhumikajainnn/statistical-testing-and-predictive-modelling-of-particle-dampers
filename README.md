# Statistical Testing and Predictive Modelling of Particle Dampers

## Overview

This project investigates the vibration reduction performance of particle dampers using statistical testing, exploratory data analysis, feature engineering, and machine learning-based predictive modelling.

The objective is to identify the parameters that most strongly influence vibration reduction and develop predictive models that can estimate the vibration reduction achieved by a particle damper for given design parameters.

## Project Objectives

* Perform statistical analysis to understand the relationship between particle-damper parameters and vibration reduction.
* Identify important parameters influencing damping performance.
* Engineer physically meaningful features from the available parameters.
* Develop and compare different machine learning regression models.
* Evaluate model performance using appropriate regression metrics.
* Identify the most influential parameters for predicting vibration reduction.

## Dataset

The dataset contains **5,000 observations** of particle-damper configurations.

### Input Parameters

* Particle Diameter (m)
* Particle Density (kg/m³)
* Number of Particles
* Enclosure Mass (kg)
* Clearance (m)
* Restitution Coefficient

### Engineered Features

* Total Particle Mass (kg)
* Particle-to-Enclosure Mass Ratio

### Target Variable

* **Vibration Reduction (%)**

The dataset is provided in the `data/` directory.

## Methodology

The project is divided into two notebooks:

### 1. Statistical Testing and Analysis

`01_Statistical_Analysis_of_Particle_Damper.ipynb`

This notebook focuses on:

* Data exploration and preprocessing
* Descriptive statistical analysis
* Distribution and skewness analysis
* Correlation analysis
* Feature engineering
* Statistical testing
* Parameter-wise and interaction analysis
* Identification of important factors affecting vibration reduction

### 2. Predictive Modelling

`02_ML_Modeling_for_Vibration_Reduction.ipynb`

This notebook develops machine learning models to predict vibration reduction.

Models investigated include:

* Linear Regression
* Random Forest Regression
* Gradient Boosting Regression

The models are evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score
* Cross-validation

## Key Results

The modelling results demonstrate that nonlinear tree-based models can capture the relationship between particle-damper parameters and vibration reduction more effectively than the linear baseline.

The analysis identified **Total Particle Mass** as the most influential engineered feature, followed by the **Restitution Coefficient**.

The final predictive modelling analysis achieved approximately:

* **R² ≈ 0.996**
* **MAE ≈ 0.45 percentage points**
* **RMSE ≈ 0.76 percentage points**

These results indicate that the developed machine learning approach can predict vibration reduction with high accuracy within the parameter range represented in the dataset.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook
* Statistical Analysis
* Machine Learning
