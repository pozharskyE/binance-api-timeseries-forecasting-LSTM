# About project
## Key task:
To predict next hour exchange rate of cryptocurrency token
## Train model (main.ipynb):
### 1. Get data
Make (multiple) request(s) to "Binance API" to get historical data about price of token (every 1 hour for last {some period})
### 2. Prepare data
Extract date, price. Save dataframe to file.
Split into training, validation, test.
Scale (normalize).
Plot
### 3. Convert array of data to timeseries X, y  (generator) 
X = token price in previous {some number of steps} hours (each hour has its own value);
y = price of token (next hour after last X)
Data is divided into batches.
### 4. Train
Keras Sequential model.
Input, LSTM and Dense layers.
### 5. Test
### 6. Save model
## Predict next hour exchange rate (predict/next_hour_forecasting.ipynb):
### Get data 
For last {some number of steps} hours
### Prepare
### Predict
Load model, predict, denormalize result
### Plot and save as png file (plot_predicted.png)
