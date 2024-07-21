# Car Price Evaluation Project

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Usage](#usage)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Preprocessing](#data-preprocessing)
- [Model Building](#model-building)
  - [Random Forest Classifier](#random-forest-classifier)
  - [Decision Tree Classifier](#decision-tree-classifier)
- [Conclusion](#conclusion)

## Overview
The Car Price Evaluation Project is designed to analyze and predict the quality of cars based on various attributes. This project uses machine learning techniques to classify cars into different categories based on their buying, maintenance cost, doors, persons capacity, lug boot size, safety, and overall class.

## Dataset
The dataset used for this project is the Car Evaluation dataset, which contains 1728 entries with 7 attributes:

- **Buying**: Buying price of the car.
- **Maintenance**: Maintenance cost.
- **Doors**: Number of doors.
- **Persons**: Capacity in terms of persons to carry.
- **Lug-Boot**: The size of the luggage boot.
- **Safety**: Estimated safety of the car.
- **Class**: Overall classification of the car (unacceptable, acceptable, good, very good).

## Usage
1. Clone the repository:
   ```
    git clone https://github.com/pranavdhawann/Car_Eval.git
    cd Car_Eval
   ```
2. Install dependencies:
   ```
    pip install -r requirements.txt
   ```

## Exploratory Data Analysis (EDA)
The initial steps involve loading the dataset and performing exploratory data analysis (EDA) to understand the data distribution and relationships between features.

## Data Preprocessing
Data preprocessing steps include:

1. Encoding categorical features.
2. Splitting the data into training and testing sets.
3. Standardizing the features.
   
## Model Building
Two machine learning models are built and evaluated in this project:

### Random Forest Classifier

A Random Forest Classifier is an ensemble learning method that constructs multiple decision trees during training and outputs the mode of the classes for classification or average prediction for regression. It improves accuracy and prevents overfitting by combining predictions from diverse, independently trained trees.

|           | Precision | Recall | F1-Score | Support |
|-----------|-----------|--------|----------|---------|
|     0     |   0.97    |  0.84  |   0.90   |    83   |
|     1     |   0.59    |  0.91  |   0.71   |    11   |
|     2     |   0.98    |  1.00  |   0.99   |   235   |
|     3     |   0.83    |  0.88  |   0.86   |    17   |

Accuracy: 0.95

### Decision Tree Classifier

A Decision Tree Classifier is a supervised learning model that predicts the target variable by learning simple decision rules inferred from data features. It partitions the data into subsets based on feature values and recursively constructs a tree structure. It's intuitive, interpretable, and prone to overfitting without pruning or regularization techniques.

|           | Precision | Recall | F1-Score | Support |
|-----------|-----------|--------|----------|---------|
|     0     |   0.99    |  0.87  |   0.92   |    83   |
|     1     |   0.62    |  0.91  |   0.74   |    11   |
|     2     |   0.98    |  1.00  |   0.99   |   235   |
|     3     |   0.82    |  0.82  |   0.82   |    17   |

Accuracy: 0.96

## Conclusion
Both the Random Forest and Decision Tree classifiers performed well, with the Decision Tree slightly outperforming the Random Forest in terms of accuracy. Further tuning and exploration of other models may yield even better results.
