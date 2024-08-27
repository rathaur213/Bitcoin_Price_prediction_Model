# Bitcoin_Price_prediction_Model


This project is a Bitcoin price prediction model built using a Long Short-Term Memory (LSTM) neural network. The model is trained on historical Bitcoin price data and is designed to predict future prices based on past trends.

## Project Overview

- **Data Source:** The historical Bitcoin price data was downloaded using the `yfinance` library, covering the period from January 1, 2015, to June 18, 2024.
- **Model Architecture:** The model is constructed using Keras and consists of four LSTM layers with varying numbers of units, followed by Dropout layers to prevent overfitting. The final layer is a Dense layer with a single unit to predict the Bitcoin price.
- **Training:** The model was trained over 50 epochs, and the loss was minimized using the mean squared error (MSE) loss function and the Adam optimizer.
- **Prediction:** After training, the model predicts Bitcoin prices for the test dataset and future days.

## Model Architecture

- **Input:** 100 days of past Bitcoin prices (scaled between 0 and 1).
- **Layers:**
  1. LSTM with 50 units and ReLU activation
  2. Dropout with a 20% rate
  3. LSTM with 60 units and ReLU activation
  4. Dropout with a 30% rate
  5. LSTM with 80 units and ReLU activation
  6. Dropout with a 40% rate
  7. LSTM with 120 units and ReLU activation
  8. Dropout with a 50% rate
  9. Dense with 1 unit
- **Output:** Predicted Bitcoin price.

## Data Preprocessing

- The data was normalized using `MinMaxScaler` to scale the prices between 0 and 1.
- Training and test datasets were split, with the last 100 days used for testing.

## Usage

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
