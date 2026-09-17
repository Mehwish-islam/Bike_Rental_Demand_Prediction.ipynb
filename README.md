# 🚲 Bike Rental Demand Prediction

## 📌 Project Overview

This project uses Machine Learning to predict the number of bikes likely to be rented on a particular day based on weather and calendar conditions.

The project uses **Linear Regression** because the target variable, `cnt`, is a continuous numerical value representing the total number of bike rentals.

The goal is to understand bike rental patterns and build a model that can predict daily bike demand under different conditions.

---

## 🎯 Project Objective

The main objective is to predict daily bike rental demand using factors such as:

- Weather conditions
- Temperature
- Humidity
- Windspeed
- Season
- Month
- Weekday
- Holiday
- Working day
- Year

This type of prediction can help bike-sharing services plan bike availability according to expected demand.

---

## 📊 Dataset

The project uses the **UCI Bike Sharing Dataset (`day.csv`)**.

The dataset contains **730 daily records** and **16 original columns**.

### Target Variable

`cnt` — Total number of bikes rented per day.

### Important Features

- `season` — Season
- `yr` — Year
- `mnth` — Month
- `holiday` — Whether the day was a holiday
- `weekday` — Day of the week
- `workingday` — Whether the day was a working day
- `weathersit` — Weather situation
- `temp` — Temperature
- `hum` — Humidity
- `windspeed` — Windspeed

---

# 🔄 Machine Learning Workflow

## Phase 1 — Problem Understanding

The problem was defined as a **regression problem** because the model needs to predict the numerical number of bikes rented per day.

The target variable is:

`cnt`

---

## Phase 2 — Dataset Exploration

The dataset was explored by checking:

- Dataset shape
- Column names
- Data types
- Statistical information
- Sample records
- Missing values

The dataset contains daily bike rental information along with weather and calendar features.

---

## Phase 3 — Data Cleaning & Preprocessing

The following preprocessing steps were performed:

- Removed the `instant` identifier column.
- Removed `casual` and `registered` to avoid data leakage because they directly contribute to the target `cnt`.
- Converted the date column.
- Checked for missing values.
- Applied one-hot encoding to categorical features.

---

## Phase 4 — Exploratory Data Analysis

Exploratory Data Analysis was performed to understand how bike rental demand changes with different conditions.

The analysis included:

- Bike rental demand over time
- Demand by season
- Demand by weather condition
- Monthly demand
- Weekday demand
- Temperature vs. bike demand

### Key Findings

The analysis showed that bike rental demand changes according to:

- Seasonal conditions
- Weather conditions
- Temperature
- Month
- Weekday and working-day patterns

---

# 🤖 Phase 5 — Linear Regression Model

Since bike rental demand is a continuous numerical value, **Linear Regression** was selected.

The dataset was divided into:

- **80% training data**
- **20% testing data**

The model was trained using the training dataset and then used to make predictions on unseen testing data.

---

# 📈 Phase 6 — Model Evaluation

The trained model was evaluated using regression metrics.

### Evaluation Metrics

| Metric | Result |
|---|---:|
| MAE | Add your Colab result |
| MSE | Add your Colab result |
| RMSE | Add your Colab result |
| R² Score | Add your Colab result |

### Metric Explanation

- **MAE:** Measures the average absolute prediction error.
- **MSE:** Measures the average squared prediction error.
- **RMSE:** Measures prediction error in approximately the same units as bike rentals.
- **R² Score:** Measures how much variation in bike rental demand is explained by the model.

---

# 🚲 Phase 7 — Bike Demand Prediction Application

An interactive prediction application was created using the trained machine learning model.

Users can enter conditions such as:

- Season
- Year
- Month
- Holiday
- Weekday
- Working day
- Weather situation
- Temperature
- Humidity
- Windspeed

The application then generates the predicted number of bikes likely to be rented.

### Example

**Input:**

Weather + temperature + humidity + calendar conditions

**Output:**

`Predicted Bike Demand: XXXX bikes`

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Google Colab
- Gradio
- GitHub

---

# 📁 Project Structure

```text
Bike-Rental-Demand-Prediction/
│
├── Bike_Rental_Demand_Prediction.ipynb
├── README.md
├── app.py
├── bike_rental_model.pkl
├── training_columns.pkl
├── requirements.txt
└── data/
    └── day.csv
