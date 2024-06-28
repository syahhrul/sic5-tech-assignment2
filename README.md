# Machine Learning for Predicting Tool Wear Failure in Milling Machines

## Overview

This project focuses on developing a machine learning model to predict tool wear failure in milling machines using sensor data. Early prediction of tool wear failure can significantly reduce production downtime and maintenance costs. The chosen model for this task is Logistic Regression, known for its simplicity, speed, and effectiveness in binary classification problems.

## Dataset

The dataset used in this project is the `ai4i2020.csv` file, which contains sensor data from milling machines. The features include various measurements such as air temperature, process temperature, rotational speed, torque, and tool wear. The target variable is the tool wear failure (`TWF`), a binary indicator of whether tool wear failure has occurred.

### Features

- `Type` : Type of machine
- `Air temperature [K]`: Temperature of the air in Kelvin.
- `Process temperature [K]`: Temperature of the process in Kelvin.
- `Rotational speed [rpm]`: Speed of the milling machine in revolutions per minute.
- `Torque [Nm]`: Torque applied during the milling process in Newton meters.
- `Tool wear [min]`: Duration of tool wear in minutes.

### Target

- `TWF`: Tool wear failure (binary: 0 for no failure, 1 for failure).

## Preprocessing

Data preprocessing includes the following steps:

1. **Standardization**: Using `StandardScaler` to normalize the features, ensuring each feature contributes equally to the model.
2. **Train-Test Split**: Splitting the data into training and testing sets with a ratio of 80:20.

## Model

### Logistic Regression

Logistic Regression is used as the primary model for this task. It is suitable for binary classification problems and provides probabilities for class membership.

### Training

The model is trained on the normalized training set using `scikit-learn`'s `LogisticRegression` implementation. Key parameters include:

- `random_state=42`: For reproducibility.
- `max_iter=1000`: To ensure convergence.

### Evaluation

The model's performance is evaluated using several metrics:

- **Accuracy**: Overall correctness of the model.
- **Classification Report**: Precision, recall, and F1-score for each class.
- **Confusion Matrix**: Detailed breakdown of true positives, false positives, true negatives, and false negatives.

### Feature Importance

The importance of each feature is analyzed using the coefficients from the Logistic Regression model. A bar chart is plotted to visualize the impact of each feature on the prediction.

## Results

The results of the model evaluation are as follows:

- **Accuracy**: 0.9945
- **Precision, Recall, F1-Score**: Detailed in the classification report.
- **Confusion Matrix**: Provides insights into the types of errors the model makes.

## Visualization

Several visualizations are created to better understand the model and its predictions:

- **Confusion Matrix**: Displayed as a heatmap for easy interpretation.
- **Feature Importance**: Visualized using a bar chart.

## Conclusion

This project demonstrates the application of Logistic Regression for predicting tool wear failure in milling machines. By leveraging sensor data, we can anticipate failures and reduce maintenance costs, leading to more efficient production processes.
