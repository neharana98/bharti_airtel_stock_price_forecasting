# Bharti Airtel Stock Price Forecasting - GRU Model
**Overview**:
Deep learning models have outperformed traditional time-series methods in forecasting complex and high-frequency financial data such as stock prices. Among these, the GRU (Gated Recurrent Unit) model, introduced by Cho et al. in 2014, offers a simplified alternative to LSTM by using fewer gates while retaining the ability to model sequential patterns in time-series data.

**Objective**:
To build a GRU model for forecasting the closing stock price of Bharti Airtel.

**Dataset**:
Using the yfinance library <https://pypi.org/project/yfinance/>, the closing price of Bharti Airtel was extracted from 27th December 2021 to 25th April 2025 (40 months). While the adjusted close price is typically preferred for stock forecasting (as it reflects corporate actions), it was unavailable for Bharti Airtel. The closing price was used instead, which was acceptable since there were virtually no significant corporate actions (splits, dividends, rights issues) during the selected period.

**Methodology**:
The data was normalised to a [0,1] scale and structured into sequences suitable for time-series modelling. A GRU-based sequential model was implemented using Keras (TensorFlow backend). Hyperparameter tuning was carried out (with epochs fixed at 20) to minimise validation loss and improve generalisation.

**Findings**:
Both training and validation losses converged quickly and remained low, indicating the model did not overfit. The GRU model captured the overall trend effectively and achieved an R-squared score of 0.816. While this is a promising result, a longer dataset (like, 10 years) would likely enhance the model's performance and forecasting accuracy.
