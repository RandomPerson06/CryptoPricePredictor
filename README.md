# ⚠️ Deprecated due to old LSTM models and major library updates causing issues.

## Overview
This tool implements an LSTM (Long Short-Term Memory) network to forecast Bitcoin prices. It uses historical daily data from Yahoo Finance to train the model and make predictions. The tool is written in Python and leverages libraries such as pandas, numpy, scikit-learn, matplotlib, and TensorFlow. Note that this tool is not intended for use as a sole indicator for investment decisions but can serve as a supplementary indicator within a broader investment strategy.

## Requirements
- pandas
- numpy (less than version 2)
- scikit-learn
- matplotlib
- tensorflow
- pandas_datareader

## Usage
- Clone the repository to your local machine.
- Install the required libraries using pip install -r requirements.txt.
- Run the code using a Python environment.

## Data
The tool fetches daily historical data of Bitcoin (BTC) against USD from Yahoo Finance. It specifically uses the 'Close' values for training and prediction. The data is scaled to the range (0, 1) using the MinMaxScaler. A look_back period of 60 days is used, meaning the model uses the past 60 days of data to predict the price 30 days ahead.

## Model
The model is a sequential LSTM network with three LSTM layers and dropout layers to prevent overfitting. It also includes a dense output layer. The model is compiled using the mean squared error loss function and the Adam optimizer. The model is trained on the training data and evaluated on the test data.

## Plot
The tool outputs a plot of the actual vs. predicted Bitcoin prices for the test period. The actual prices are shown in black, and the predicted prices are shown in green.

## Detailed Description
This script uses the LSTM (Long Short-Term Memory) algorithm in the Keras library to predict Bitcoin prices. The prices are fetched from Yahoo Finance and preprocessed using pandas and scikit-learn. The 'Close' values are scaled and reshaped for training the LSTM model.

The script performs the following steps:

1. Import necessary libraries.
2. Fetch historical price data from Yahoo Finance.
3. Scale and preprocess the data.
4. Split the data into training and test sets.
5. Create and train the LSTM model.
6. Use the trained model to make predictions.
7. Plot the actual and predicted prices.
8. Print the prediction for the next day.
9. The LSTM model consists of three LSTM layers with 50 units each and dropout layers to prevent overfitting. The model uses a look_back period of 60 days to predict the price 30 days into the future. After training, the model's predictions are plotted against the actual prices for visual comparison.
