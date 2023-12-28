# New York City Taxi Fare Prediction

This repository provides a holistic solution for predicting taxi fares in New York City, employing a stack of four distinct machine learning models. The dataset used is the New York City Taxi Fare Prediction dataset, accessible on Kaggle [here](https://www.kaggle.com/c/new-york-city-taxi-fare-prediction).

## Overview

The primary goal of this project is to predict the fare amount for taxi rides in New York City. The prediction is based on various features such as pickup and dropoff locations, date and time of pickup, and the number of passengers. The included code covers data preprocessing, exploratory data analysis, feature engineering, and the implementation of machine learning models for prediction.

## Setup

Before running the code, make sure to set up your environment and download the dataset by following these steps:

1. Install the Kaggle library and configure it with your Kaggle API credentials. Ensure you have a Kaggle account and generate your API token as `kaggle.json`.

```python
!pip install -q kaggle
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
```

2. Download the dataset from Kaggle using the Kaggle CLI:

```python
!kaggle competitions download -c new-york-city-taxi-fare-prediction
```

3. Unzip the downloaded dataset:

```python
!unzip new-york-city-taxi-fare-prediction.zip
```

4. Remove unnecessary files:

```python
!rm /content/new-york-city-taxi-fare-prediction.zip
!rm /content/GCP-Coupons-Instructions.rtf
!rm /content/sample_submission.csv
```

## Data Exploration and Preprocessing

The code covers data exploration and preprocessing steps, including:

- Loading the dataset and inspecting its structure.
- Handling missing values and outliers.
- Visualizing the distribution of key features.
- Creating new features based on date and time.

## Feature Engineering

Feature engineering is a crucial part of the data preparation process. In this project, the code creates new features, such as:

- Calculating the distance between pickup and dropoff locations.
- Extracting datetime features like hour, date, month, year, and day of the week.

## Machine Learning Models

The code implements four machine learning models for predicting taxi fares:

1. Random Forest Regressor
2. XGBoost Regressor
3. LightGBM Regressor
4. Stacked Model

The models are trained, evaluated, and the root mean squared error (RMSE) is used as the evaluation metric. The stacked model combines predictions from Random Forest, XGBoost, and LightGBM models.

## Data Cleaning and Preprocessing

Data cleaning and preprocessing steps are pivotal for preparing the dataset for modeling. The code includes:

- Removing instances with negative fare amounts.
- Removing instances with fare outliers.
- Filtering instances based on longitude and latitude boundaries.
- Eliminating instances with zero distance and zero fare.
- Cleaning passenger count values.
- Handling distance outliers.
- Normalizing the fare amount using the natural logarithm.

## Model Evaluation

The code evaluates the performance of each machine learning model and calculates the RMSE. It also demonstrates how to stack multiple models for potentially improved predictive performance.

## Conclusion

This repository serves as a comprehensive guide for addressing a taxi fare prediction problem using machine learning. Feel free to use this code as a starting point for your projects and explore ways to enhance model performance and feature engineering.

For any questions or suggestions, please don't hesitate to reach out. Happy coding!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Feel free to use and modify the code for your own projects or educational purposes. If you find this repository helpful, please consider giving it a star!