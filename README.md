# Stock Forecast App

## Overview

The Stock Forecast App is a Streamlit application that allows users to visualize historical stock prices and forecast future stock prices using machine learning. This app leverages the `yfinance` library to retrieve stock data, `Prophet` by Facebook for forecasting, and `Plotly` for interactive visualizations. The application provides an intuitive interface for selecting stocks, adjusting prediction periods, and exploring forecasted results.

## Features

- **Stock Selection**: Choose from a predefined list of stocks to analyze.
- **Forecast Range**: Adjust the number of years for which you want to predict future stock prices.
- **Interactive Data Visualization**: View historical stock data and forecast results with interactive Plotly charts.
- **Forecast Analysis**: Examine the different components of the forecast, including trends and seasonal patterns.

## Requirements

To run this app, you will need Python 3.7 or higher. The following Python libraries are required:

- `streamlit`: For creating the web application interface.
- `yfinance`: For fetching historical stock data.
- `plotly`: For interactive plotting.
- `prophet`: For time series forecasting.

You can install these dependencies using the `requirements.txt` file provided.

## Installation

1. **Clone the Repository**

    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Create and Activate a Virtual Environment**

    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install Required Packages**

    Create a `requirements.txt` file with the following content:

    ```txt
    streamlit
    yfinance
    plotly
    prophet
    ```

    Install the packages:

    ```sh
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Streamlit Application**

    Navigate to the directory containing `t80.py` and run the Streamlit app using the following command:

    ```sh
    streamlit run YouTrade.py
    ```

2. **Interact with the Application**

    - **Select a Stock**: Use the dropdown menu to choose a stock from the available options (`MSFT`, `TSLA`, `GOOG`, `AAPL`, `NVDA`).
    - **Adjust Prediction Range**: Use the slider to select the number of years for forecasting. The app will generate predictions for the selected period.
    - **View Historical Data**: The app displays the raw historical stock data.
    - **Explore Forecasts**: The app provides interactive plots for both historical and forecasted stock prices.
    - **Analyze Forecast Components**: View the various components of the forecast, such as trends and seasonality.

## Code Explanation

### Imports

```python
from datetime import date
import streamlit as st
import yfinance as yf
from plotly import graph_objs as go
from prophet import Prophet
from prophet.plot import plot_plotly
