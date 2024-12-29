# Predictive Model for Maximizing User Engagement with CTA Banners

## Overview
This project focuses on building a predictive machine learning model to optimize user engagement on a website through targeted call-to-action (CTA) banners. The goal is to predict the probability of a user clicking on a CTA banner (ClickedCTA) based on given features. The model utilizes historical data and aims to maximize key metrics through thoughtful feature engineering and model evaluation.

## Dataset
The dataset consists of two files:
- `train.csv`: Contains 100,000 rows of labeled data for training.
- `test.csv`: Contains 20,000 rows of unlabeled data for making predictions.

The features include demographic, behavioral, and contextual data points influencing user behavior. The target variable, `ClickedCTA`, is binary (0 or 1).

## Methodology

### Data Preprocessing
1. **Train-Test Split:** The data is split into training and validation sets using an 80-20 ratio.
2. **Feature Scaling:** To ensure uniformity, features such as `Income` were standardized using `StandardScaler`.

### Model Architecture
A neural network model was implemented using TensorFlow and Keras. The architecture is as follows:
- Input layer: Handles scaled features.
- Hidden layers: Three fully connected layers with ReLU activation and dropout for regularization.
- Output layer: A single neuron with sigmoid activation to predict the probability of `ClickedCTA`.

The model was trained using:
- Optimizer: Stochastic Gradient Descent (SGD) with a learning rate of 0.001.
- Loss Function: Binary Cross-Entropy, to measure prediction accuracy.
- Early stopping to prevent overfitting by monitoring validation loss.

### Evaluation Metrics
The model was evaluated on the following metrics:
- **Log Loss:** The primary evaluation metric emphasizes prediction confidence.
- **Precision, Recall, and F1 Score:** Additional metrics to measure classification performance.

### Results
- **Validation Log Loss:** 0.1028
- **Precision:** 1.00
- **Recall:** 0.862
- **F1 Score:** 0.926

## Visualizations
To enhance interpretability, the notebook includes visualizations of:
- Feature importance.
- Model loss across training epochs.
- Confusion matrices for classification performance.

## Repository Contents
- `train.csv` and `test.csv`: Data files used for training and testing.
- `technical.ipynb`: Jupyter Notebook containing the full code, analysis, and visualizations.

## Usage
This repository is intended to demonstrate machine learning techniques and model evaluation. Portions of the code critical to prediction generation have been omitted to ensure responsible sharing. Users are encouraged to experiment with the methodology and adapt it to similar tasks.

## Disclaimer
This project is intended for demonstration and educational purposes only. Any commercial use, redistribution, or use for competitive purposes is strictly prohibited without prior permission. 
