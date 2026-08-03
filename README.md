# Stock-predictor-
📈 Stock ML Predictor
An ML-powered stock analysis dashboard built with Streamlit. Fetches historical + real-time stock data, computes 20 technical indicators, and trains regression models to forecast future prices.
Features
Live data — Alpha Vantage API (free tier) with automatic yfinance fallback, so it works even without an API key
Technical analysis — Candlestick charts, Moving Averages, RSI, MACD, Bollinger Bands, historical volatility
4 ML models — Linear Regression, Random Forest, Gradient Boosting, SVR
Model evaluation — R², MAE, RMSE, MAPE on a held-out test set, plus actual-vs-predicted and residual plots
Feature importance — See which technical indicators drive each prediction
10 popular tickers pre-loaded (AAPL, GOOGL, MSFT, TSLA, RELIANCE.NS, TCS.NS, etc.) plus custom symbol input
Tech Stack
Frontend/App: Streamlit
Data: Alpha Vantage API, yfinance
ML: scikit-learn
Visualization: Plotly
Project Structure
Code
Setup & Run
Clone the repo
Bash
Install dependencies
Bash
Run the app
Bash
(Optional) Get a free Alpha Vantage API key at alphavantage.co and paste it in the sidebar. Without a key, the app automatically uses yfinance (also free, no signup).
How It Works
Fetch — Pulls OHLCV history and a live quote for the selected symbol
Feature Engineer — Computes 20 technical indicators (MAs, EMAs, MACD, RSI, Bollinger Bands, returns, volatility, volume ratios, candle shape)
Train — Splits data chronologically (80/20, no shuffle — correct for time series), scales features, trains the selected model
Predict — Forecasts closing price N days ahead with a BUY/SELL signal based on predicted direction
Evaluate — Reports R², MAE, RMSE, MAPE and visualizes actual vs. predicted values plus residuals
Disclaimer
This project is for educational purposes only. Predictions are based on historical technical indicators and should not be used as financial advice.
Author
Built by Yash — B.Tech IT, Rungta College of Engineering and Technology, Bhilai
