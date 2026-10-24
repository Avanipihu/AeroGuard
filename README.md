# AeroGuard: Aircraft Engine Remaining Useful Life Prediction

## Project Overview

AeroGuard is a machine learning project focused on predicting the Remaining Useful Life (RUL) of aircraft engines using regression and ensemble learning algorithms. The project uses the NASA C-MAPSS Turbofan Engine Degradation Simulation Dataset to study engine degradation and estimate the number of operating cycles remaining before an engine reaches the end of its useful life. The study compares ten regression algorithms using a common dataset and evaluation framework to understand their predictive performance and suitability for predictive maintenance.

## Problem Statement

Aircraft engines undergo gradual wear and degradation during operation. If this degradation is not detected in time, it can result in unexpected failures, increased maintenance costs, and safety risks. Predicting the remaining useful life of an engine helps estimate when maintenance may be required and supports more effective maintenance planning. AeroGuard investigates how different regression and ensemble learning techniques can estimate engine RUL and identifies suitable models based on their actual prediction performance.

## Objectives

The primary objective of AeroGuard is to implement and evaluate multiple regression algorithms for predicting the remaining useful life of aircraft engines. The project aims to compare their performance using appropriate regression metrics, identify models that provide accurate predictions, and understand the strengths and limitations of individual regression methods and ensemble learning techniques in predictive maintenance.

## Dataset

The project uses the NASA C-MAPSS Turbofan Engine Degradation Simulation Dataset, specifically the FD004 subset. This dataset contains simulated aircraft engine operating conditions and sensor measurements collected over multiple operating cycles. It provides information that can be used to study engine degradation patterns and develop machine learning models for remaining useful life prediction.

The dataset can be accessed through the following sources:

**Dataset Download:** [NASA C-MAPSS Turbofan Engine Degradation Simulation Dataset](https://phm-datasets.s3.amazonaws.com/NASA/6.+Turbofan+Engine+Degradation+Simulation+Data+Set.zip)

**Official NASA Repository:** [NASA Prognostics Center of Excellence Data Set Repository](https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/)


## Machine Learning Algorithms

AeroGuard evaluates ten regression algorithms to compare different approaches to remaining useful life prediction. Simple Linear Regression establishes a baseline by modelling the relationship between an input feature and RUL, while Multiple Linear Regression uses multiple input features to estimate the target value. Ridge Regression applies regularization to reduce the effect of large coefficients, and Lasso Regression uses regularization that can also reduce less useful feature coefficients to zero.

The Generalized Linear Model provides a flexible regression framework based on a specified distribution and link function. Support Vector Regression estimates continuous target values by learning a function that limits prediction errors within a defined tolerance.

The ensemble learning algorithms include Bagging Regressor, which combines predictions from multiple models to improve stability; AdaBoost Regressor, which sequentially emphasizes observations that are difficult to predict; Gradient Boosting Regressor, which builds an additive model by correcting previous prediction errors; and XGBoost Regressor, which implements an optimized gradient-boosting approach for regression tasks.

## Implementation Tools and Technologies

The project is implemented in Python using Jupyter Notebook. Pandas and NumPy are used for dataset handling, data manipulation, and numerical computations. Matplotlib and Seaborn support exploratory data analysis and visualization. Scikit-learn provides the regression algorithms, preprocessing utilities, and evaluation metrics, while XGBoost is used to implement the XGBoost regression model. The NASA C-MAPSS dataset serves as the primary data source for training and evaluating the models.

## Evaluation Metrics

The performance of the regression algorithms is evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and the coefficient of determination (R²). MAE measures the average absolute difference between predicted and actual RUL values, while RMSE gives greater weight to larger prediction errors. The R² score measures how well a model explains the variation in the target values relative to a baseline.

Lower MAE and RMSE values generally indicate more accurate predictions, while a higher R² score generally indicates better explanatory performance. These metrics are used together to compare the prediction accuracy and limitations of the ten regression algorithms.

## Expected Results and Analysis

The experimental analysis compares all ten regression algorithms using MAE, RMSE, and R². Tables and visualizations are used to present the results and highlight differences between individual regression models and ensemble learning techniques. The analysis focuses on identifying which algorithms provide lower prediction errors and more reliable RUL estimates on the validation data.

The final conclusions are based on the actual experimental results rather than assumed performance values. The selected model is assessed according to its prediction accuracy and suitability for aircraft engine predictive maintenance.
