# Blood Glucose Forecasting
This project is aimed at predicting blood glucose levels using a machine learning approach. The model leverages the Random Forest algorithm, which is known for its ability to handle complex datasets effectively and provide robust predictions. This project demonstrates data preprocessing, model training, and evaluation, as well as a way to save and deploy the trained model for real-world use.


## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)
- [Usage](#usage)
- [License](#license)

## Introduction
Blood glucose level forecasting is crucial for managing conditions like diabetes. Accurate predictions can assist individuals and healthcare providers in making timely decisions to prevent glucose spikes or dips. This project utilizes a supervised learning model with the Random Forest algorithm to predict glucose levels based on historical data and various influencing factors.

## Dataset
The dataset contains various features related to blood glucose levels, such as:
- **Glucose**: Blood glucose level (mg/dL)
- **Blood Pressure**: Blood pressure level (mmHg)
- **Skin Thickness**: Thickness of skin (mm)
- **Insulin**: Insulin level (µU/mL)
- **BMI**: Body Mass Index (weight in kg/(height in m)^2)
- **DPF**: Diabetes Pedigree Function - likelihood of diabetes based on family history
- **Age**: Age of the individual

  ```bash
  .├── data/                      # Dataset (CSV files)
   ├── notebooks/                 # Jupyter notebooks with experiments
   ├── models/                    # Saved model files (.pkl)
   ├── src/                       # Source code
   │   ├── data_preprocessing.py  # Data cleaning and preprocessing scripts
   │   ├── model_training.py      # Model training and evaluation scripts
   │   └── predict.py             # Script for loading and using the trained model
   ├── README.md                  # Project documentation
   └── requirements.txt           # Required libraries

## Installation
To get started with this project, clone the repository and install the dependencies.


    git clone https://github.com/yourusername/blood-glucose-forecasting.git
    cd blood-glucose-forecasting
    pip install -r requirements.txt

## Data Preprocessing
The preprocessing steps are essential for preparing the data for model training:

- Data Cleaning: Replace invalid values (e.g., zeros) in specific columns (Glucose, Blood Pressure, Skin Thickness, Insulin, BMI) with NaN, then fill NaN values with mean or median depending on the feature's distribution.
- Feature Selection: Select relevant features that contribute to blood glucose forecasting.
  
## Model Training
The Random Forest model is trained on the preprocessed data to forecast blood glucose levels. The following steps are involved:

- Splitting the data into training and testing sets (80% training, 20% testing).
- Training the Random Forest model with selected hyperparameters.
- Saving the trained model as diabetes-prediction-rfc-model.pkl for later use.

## Model Evaluation
After training, the model's performance is evaluated using standard metrics:

- Accuracy
- Precision
- Recall
- Confusion Matrix
These metrics provide insight into the model's predictive capabilities and help in refining the model.
