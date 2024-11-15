# House Price Prediction using Linear, Ridge, and Lasso Regression

## Overview
This task aims to predict house prices based on key features such as square footage, number of bedrooms, bathrooms, and other relevant attributes. We implement three regression models: **Linear Regression**, **Ridge Regression** (with L2 regularization), and **Lasso Regression** (with L1 regularization). The models are evaluated using cross-validation to determine which provides the best prediction.

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Installation and Setup](#installation-and-setup)
- [Dataset](#dataset)
- [Feature Engineering](#feature-engineering)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Results and Visualization](#results-and-visualization)

## Project Structure
```sh
.
├── train.csv               # Training dataset
├── test.csv                # Test dataset
├── house_price_prediction.py  # Main Python script for model implementation
├── README.md               # This README file
```

## Installation and Setup

### 1. Clone the Repository
First, clone the repository to your local machine:
```sh
git clone https://github.com/abigiyaayele/PRODIDY_ML_01.git
cd PRODIDY_ML_01
```

### 2. Install Dependencies
Make sure you have Python 3.7+ installed. Install the necessary packages using \`pip\`:

```sh
pip install -r requirements.txt
```

The \`requirements.txt\` should include:
```sh
numpy
pandas
scikit-learn
matplotlib
```

### 3. Dataset
The dataset used in this project is sourced from the [Kaggle House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data).

## Feature Engineering
The key features used for prediction are:
- **GrLivArea**: Above-ground living area (square feet)
- **BedroomAbvGr**: Number of bedrooms above ground
- **FullBath**: Number of full bathrooms
- **OverallQual**: Overall material and finish quality of the house
- **YearBuilt**: Year the house was built
- **GarageArea**: Area of the garage in square feet

Missing values in these features are filled with the mean of the column, and data is scaled using \`StandardScaler\`.

## Model Training and Evaluation

### 1. **Linear Regression**
A basic linear regression model is trained on the selected features to predict house prices. This model serves as the baseline for further comparison.

### 2. **Ridge Regression**
Ridge regression applies L2 regularization to penalize large coefficients, reducing overfitting and improving generalization, particularly when dealing with multicollinearity in features.

### 3. **Lasso Regression**
Lasso regression introduces L1 regularization, which helps in both preventing overfitting and performing feature selection by shrinking some feature coefficients to zero.

### 4. **Cross-Validation**
We use 5-fold cross-validation to evaluate model performance in a more robust manner. The performance metric used is **Root Mean Squared Error (RMSE)**, which measures the differences between predicted and actual values.

## Results and Visualization

### Model Comparison
After training, the models are compared based on **RMSE**. The lower the RMSE, the better the model performance.

| Model           | Cross-Validation RMSE |
|-----------------|-----------------------|
| Linear Regression |  39528.78803288624 |
| Ridge Regression  |  39526.85385485418 |
| Lasso Regression  |  39528.78417950614 |

### Visualization of Actual vs Predicted Prices
A scatter plot is generated to visualize the relationship between the predicted house prices and the actual prices for the linear regression model:

## Conclusion
In this task, Linear regression and regularization techniques (Ridge and Lasso) was implemented to predict house prices. Cross-validation was used to select the best-performing model based on RMSE, and the relationship between actual and predicted prices was visualized for a deeper understanding of model performance.
