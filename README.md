## README.md

# neural-network-challenge-2
Module 19

# Attrition Data Analysis and Prediction

This project involves analyzing and predicting employee attrition and department classification using a neural network model. The dataset contains various features related to employee demographics, job roles, and satisfaction levels. The goal is to build a model that can accurately predict employee attrition and classify the department they belong to.

## Table of Contents
1. [Installation](#installation)
2. [Data Preprocessing](#data-preprocessing)
3. [Model Architecture](#model-architecture)
4. [Training the Model](#training-the-model)
5. [Evaluation](#evaluation)
6. [Conclusion](#conclusion)

## Installation

To run this project, ensure you have the following libraries installed:

- pandas
- numpy
- scikit-learn
- tensorflow

You can install these packages using pip:

```bash
pip install pandas numpy scikit-learn tensorflow
```

## Data Preprocessing

1. **Loading the Data**: The dataset is loaded from a CSV file. The first few rows and the unique values for each column are displayed to understand the data.

2. **Feature Selection**: Selected 10 features related to employee demographics and job satisfaction for model input.

3. **Encoding Categorical Variables**: Used `LabelEncoder` for binary encoding of the 'OverTime' feature and `OneHotEncoder` for multi-class encoding of 'Department' and 'Attrition' columns.

4. **Data Splitting**: Split the data into training and testing sets using `train_test_split`.

5. **Feature Scaling**: Applied `StandardScaler` to normalize the features.

## Model Architecture

The model consists of a shared input layer followed by two dense layers. It branches into two separate heads:

- **Department Classification Head**: Includes a dense layer and an output layer with a softmax activation function for multi-class classification.
- **Attrition Prediction Head**: Includes a dense layer and an output layer with a sigmoid activation function for binary classification.

The model is compiled with the Adam optimizer and different loss functions for each output: `categorical_crossentropy` for the department and `binary_crossentropy` for attrition.

## Training the Model

The model is trained for 100 epochs with a batch size of 32. The training process includes logging the loss and accuracy for both outputs.

## Evaluation

The model's performance is evaluated using the testing dataset. The accuracy for both department classification and attrition prediction is displayed.

## Conclusion

- **Model Performance**: The model achieved a certain level of accuracy for both department and attrition predictions. However, accuracy may not be the best metric due to potential class imbalance.

- **Activation Functions**: The softmax activation function was used for department classification (multi-class), while sigmoid was used for attrition prediction (binary).

- **Improvements**: The model can be improved by better encoding of categorical variables, increasing model complexity, and handling class imbalances.

## Summary

This project demonstrates a basic approach to predicting employee attrition and department classification using neural networks. Future work can explore more advanced models and techniques to improve accuracy and robustness.
