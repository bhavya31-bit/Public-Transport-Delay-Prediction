# 🚌 Public Transport Delay Prediction System

## 📌 Overview

This project implements a **machine learning–based public transport delay prediction system** using historical bus operation data. A **Random Forest Regressor** is trained to predict the expected delay (in minutes) based on observable features such as route, day, hour, and service gap.

An interactive **Gradio web application** is included to allow users to make real-time delay predictions.


## 🎯 Objectives

- Predict bus delays using historical transport data
- Apply proper feature engineering and data cleaning
- Train a well-optimized Random Forest regression model
- Visualize actual vs predicted delay values
- Deploy a simple web interface for user interaction


## 📊 Dataset Description

The dataset contains historical public transport records used to predict service delays.

### Features Used

| Column Name | Description |
|------------|------------|
| Route | Bus route number |
| Day | Day of operation |
| Hour | Extracted hour from scheduled time |
| Min Gap | Time gap between consecutive services (minutes) |
| Min Delay | Actual delay in minutes (target variable) |

### Target Variable

- **Min Delay**
  - `0` → On time  
  - `> 0` → Delayed  
  - Negative values are removed during preprocessing
  - 

## 🧠 Data Preprocessing & Feature Engineering

- Converted time into hourly format
- Removed missing and invalid records
- Clipped negative delay values
- Ensured **Min Gap** values are non-negative
- Encoded categorical variables using `LabelEncoder`
- Removed leakage-prone and unstable features


## 🤖 Machine Learning Model

- **Algorithm:** Random Forest Regressor
- Handles non-linear relationships effectively
- Robust to noise and categorical encodings


## 📈 Model Evaluation

The model is evaluated using:

- **Mean Absolute Error (MAE)**
- **Actual vs Predicted Delay Scatter Plot**

Lower MAE indicates better prediction accuracy.


## 🌐 Web Application (Gradio)

An interactive web interface is implemented using **Gradio**.

### User Inputs

- Route
- Day
- Hour (0–23)
- Minimum service gap (non-negative)

### Output

- Predicted delay in minutes

