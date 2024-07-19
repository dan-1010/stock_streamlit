# Stock Streamlit Predictor

This project is a Stock Market Predictor application built using Python. It allows users to input a stock symbol and view various visualizations of the stock's historical data, including moving averages and predicted prices. The model used for prediction is pre-trained and loaded from a file. The application is built using the Streamlit library for a simple and interactive web interface.

## Features

- **Input Stock Symbol:** Users can enter any stock symbol to fetch and display historical data.
- **Display Stock Data:** Shows historical stock data from Yahoo Finance.
- **Visualize Moving Averages:** Plots 50-day, 100-day, and 200-day moving averages.
- **Predict Stock Prices:** Uses a pre-trained model to predict future stock prices and visualize the results against the original prices.

## Prerequisites

- Python 3.x
- Required Python libraries:
  - numpy
  - pandas
  - yfinance
  - keras
  - streamlit
  - matplotlib
  - scikit-learn

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/stock-market-predictor.git
    cd stock-market-predictor
    ```

2. Install the required libraries:
    ```sh
    pip install numpy pandas yfinance keras streamlit matplotlib scikit-learn
    ```

3. Ensure you have the pre-trained model file `stock_prediction_model.keras` and place it in the appropriate directory.

## Usage

1. Run the Streamlit application:
    ```sh
    streamlit run app.py
    ```

2. Enter the stock symbol (e.g., `SBIN.NS`) in the input field on the web interface.

3. View the historical stock data and various visualizations:
    - Stock data
    - Price vs 50-day moving average
    - Price vs 50-day and 100-day moving averages
    - Price vs 100-day and 200-day moving averages
    - Original price vs predicted price

## Code Overview

### Importing Libraries

```python
import numpy as np
import pandas as pd
import yfinance as yf
from keras.models import load_model
import streamlit as st
import matplotlib.pyplot as plt
from sklearn.preprocessing import MinMaxScaler