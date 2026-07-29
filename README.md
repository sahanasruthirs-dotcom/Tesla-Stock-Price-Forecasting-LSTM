# 📈 Tesla Stock Price Forecasting Using LSTM

## Project Overview

This project demonstrates stock price forecasting using a Long Short-Term Memory (LSTM) neural network. The model learns historical Tesla stock price patterns and predicts future closing prices.

The project is implemented using Python, TensorFlow/Keras, Pandas, NumPy, Matplotlib, and Scikit-learn.

---

## Dataset

Dataset: Tesla Historical Stock Prices

Features:
- Date
- Open
- High
- Low
- Close
- Volume

Target Variable:
- Close Price

---

## Technologies Used

- Python
- TensorFlow
- Keras
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

## Data Preprocessing

The following preprocessing steps were performed:

- Removed missing values
- Selected Closing Price
- Normalized data using MinMaxScaler
- Created 60-day sequences
- Split data into training and testing datasets

---

## LSTM Model Architecture

Input Layer

↓

LSTM Layer (50 Units)

↓

Dropout (20%)

↓

LSTM Layer (50 Units)

↓

Dropout (20%)

↓

Dense Layer (25 Units)

↓

Output Layer (1 Unit)

---

## Performance Metrics

The model was evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

---

## Results

The predicted stock prices closely follow the actual stock prices.

Visualizations include:

- Stock Price Trend
- Training Loss
- Actual vs Predicted Prices

---

## Future Improvements

- Bidirectional LSTM
- GRU
- Hyperparameter Optimization
- Attention Mechanism
- Technical Indicators
- Sentiment Analysis

---

## How to Run

1. Clone the repository

2. Install dependencies

pip install -r requirements.txt

3. Open Jupyter Notebook

4. Run all cells

---

## Author

Sahana Sruthi R.S.
