# Tesla Stock Price Forecasting Using LSTM

A deep learning project that forecasts Tesla's closing stock price with a Long Short-Term Memory (LSTM) neural network trained on historical price data.

## Overview
Stock prices are time-series data, so past values carry information about future movement. This project learns patterns from the previous 60 days of closing prices and predicts the next closing price. Predictions are compared with actual prices using error metrics and plots.

## Technologies Used
- Python
- TensorFlow / Keras: LSTM model
- Pandas and NumPy: data handling
- Scikit-learn: scaling and evaluation metrics
- Matplotlib: visualization
- Jupyter Notebook

## Dataset
Tesla historical stock prices with these columns: `Date`, `Open`, `High`, `Low`, `Close`, `Volume`.
- **Target variable:** `Close` price

## Implementation Details
### 1. Data preprocessing
- Removed missing values
- Selected the closing price
- Normalized values with `MinMaxScaler`
- Created sliding-window sequences of 60 days
- Split the data into training and testing sets

### 2. Model architecture
```
Input
  ↓
LSTM (50 units)
  ↓
Dropout (20%)
  ↓
LSTM (50 units)
  ↓
Dropout (20%)
  ↓
Dense (25 units)
  ↓
Output Dense (1 unit)
```

### 3. Training and evaluation
The model is trained on the training sequences, and its predictions are converted back to the original price scale. It is evaluated with:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

## Results
The predicted prices follow the actual price trend closely. The notebook includes:
- Stock price trend over time
- Training loss curve
- Actual vs predicted closing prices

Add your screenshots to an `images/` folder and reference them here:
```
![Actual vs Predicted](images/actual_vs_predicted.png)
```

## Project Structure
```
Tesla-Stock-Price-Forecasting-LSTM/
├── <notebook>.ipynb     # Data preprocessing, model training and evaluation
├── requirements.txt     # Python dependencies
└── README.md
```

## Setup Instructions
```bash
git clone https://github.com/sahanasruthirs-dotcom/Tesla-Stock-Price-Forecasting-LSTM.git
cd Tesla-Stock-Price-Forecasting-LSTM
pip install -r requirements.txt
```

## Usage
1. Start Jupyter: `jupyter notebook`
2. Open the notebook and make sure the Tesla stock CSV file path in the data-loading cell is correct.
3. Run all cells from top to bottom to preprocess data, train the model and view the plots.

## Limitations
Stock prices depend on many external factors that price history alone cannot capture. This project is for learning and experimentation and is not financial advice.

## Future Improvements
- Bidirectional LSTM and GRU models
- Hyperparameter optimization
- Attention mechanism
- Technical indicators as extra features
- Sentiment analysis of news

## Author
**Sahana Sruthi R.S.** · B.Tech CSE (AI & Data Analytics)
[LinkedIn](https://www.linkedin.com/in/sahana-sruthi-r-s-4612b4315) · [Portfolio](https://sahanasruthirs-dotcom.github.io)
