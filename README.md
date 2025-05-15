# bharti_airtel_stock_price_forecasting
**Overview**:
Deep Learning models have taken the lead over traditional time-series models, given their accuracy, even when dealing with complex and high-frequency financial data like stock prices. The GRU (Gated Recurrent Unit) model was introduced in 2014 by Cho et al. as a simpler alternative (with fewer gates) to the LSTM (Long Short-Term Memory) model. GRU and LSTM models, both types of RNN (Recurrent Neural Network) architectures, are primarily used for time series data to make predictions based on patterns in the ordered inputs.

**Objective**:
To build a GRU model for forecasting the stock price of Bharti Airtel.

**Dataset**:
From finance <https://pypi.org/project/yfinance/>, extracted the closing price of Bharti Airtel in the past 40 months -- from 27th December 2021 to 25th April 2025.
I intended to use the adjusted close price — typically preferred over the close price in stock price forecasting, given it accounts for corporate actions like dividends, stock splits, and rights offerings, thereby allowing it to provide a better reflection of the stock’s value over time. However, since the Adjusted Close data was not available for Bharti Airtel via yfinance, I settled with the Close price--acceptable since there were virtually no stock splits, rights issue of equity shares, and dividend payouts during this period.

**Methodology**:
