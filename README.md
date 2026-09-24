# Polynomial Regression for Rod Temperature Distribution

## Overview

This project investigates the use of **polynomial regression** to approximate the temperature distribution along a one-dimensional rod.

The objective is to compare polynomial approximations with the analytical temperature solution and study how the quality of the approximation changes with different levels of measurement noise.

The project uses a small dataset of randomly selected points along a rod of unit length and evaluates the regression model using separate training and testing datasets.

## Problem Statement

Consider a rod of total length

$$
L = 1
$$

with thermal conductivity

$$
k = 3
$$

and heat-generation parameter

$$
q_0 = 20.
$$

Temperature values are generated at 30 randomly selected locations along the rod. The dataset is divided into:

* **80% training data**
* **20% testing data**

Polynomial regression models are then trained to approximate the temperature distribution.

The experiment is repeated for different levels of noise to investigate the effect of noisy observations on the regression model.

## Objectives

The main objectives are:

1. Generate temperature data from the analytical solution.
2. Randomly select 30 points along the rod.
3. Divide the data into training and testing sets.
4. Implement polynomial regression.
5. Fit polynomials of different degrees to the training data.
6. Compare predictions with the analytical temperature solution.
7. Study the effect of noise on model accuracy.
8. Evaluate the models using regression error metrics and visualizations.

## Methodology

The workflow used in this project is:

```text
Analytical temperature solution
            ↓
Generate spatial data points
            ↓
Add measurement noise
            ↓
Train/Test split (80/20)
            ↓
Polynomial feature generation
            ↓
Polynomial regression
            ↓
Prediction
            ↓
Error evaluation
            ↓
Comparison with analytical solution
```

## Polynomial Regression

A polynomial regression model of degree \(n\) has the form

$$
T(x) =
\beta_0 +
\beta_1x +
\beta_2x^2 +
\cdots +
\beta_nx^n.
$$

The coefficients are estimated using the training data.

Different polynomial degrees can be investigated to observe the trade-off between underfitting and overfitting.

## Experimental Setup

| Parameter                         |                 Value |
| --------------------------------- | --------------------: |
| Rod length                        |                     1 |
| Thermal conductivity \(k\)        |                     3 |
| Heat-generation parameter \(q_0\) |                    20 |
| Number of data points             |                    30 |
| Training fraction                 |                   80% |
| Testing fraction                  |                   20% |
| Sampling                          |                Random |
| Model                             | Polynomial Regression |

## Noise Analysis

To examine the robustness of polynomial regression, noise is added to the generated temperature measurements.

The fitted polynomial is compared against the analytical solution for different noise levels.

This allows the following questions to be investigated:

* How accurately can polynomial regression recover the temperature field?
* How does increasing noise affect the fitted polynomial?
* Which polynomial degree provides a suitable approximation?
* Does a higher-degree polynomial necessarily provide better generalization?

## Evaluation

The model can be evaluated using metrics such as:

* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* Mean Absolute Error (MAE)
* \(R^2\) score

Visual comparisons are also used to compare:

1. Analytical temperature distribution
2. Noisy observations
3. Polynomial regression predictions

## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── notebooks/
│   └── polynomial_regression_temperature.ipynb
├── src/
│   └── polynomial_regression.py
└── results/
    ├── figures/
    └── metrics.csv
```

## Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/polynomial-regression-rod-temperature.git
cd polynomial-regression-rod-temperature
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

## Running the Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
notebooks/polynomial_regression_temperature.ipynb
```

The notebook contains the complete experiment, including data generation, model fitting, prediction, evaluation, and visualization.

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## Results

The results section compares polynomial approximations with the analytical temperature solution under different noise conditions.

Representative plots include:

* Analytical temperature distribution
* Training and testing data
* Polynomial fits of different degrees
* Effect of measurement noise
* Model error comparison

## Key Learning Outcomes

This project demonstrates:

* Polynomial feature transformation
* Regression model fitting
* Train-test splitting
* Model evaluation
* Bias-variance trade-off
* Overfitting and underfitting
* Effect of noise on regression
* Numerical approximation of a physical system

## Author

**Apoorva Singh**

Deep Learning Coursework

2025MEM1003
