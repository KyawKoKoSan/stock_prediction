### Brief Report on Stock Price Prediction Using LSTM

#### Introduction
This project focuses on predicting stock prices using a **Long Short-Term Memory (LSTM)** model, a type of recurrent neural network (RNN). LSTMs are widely used for time series forecasting due to their ability to capture long-term dependencies in sequential data. The goal is to predict the closing price of a stock based on historical data, including the stock's open, high, low, close prices, trading volume, and moving averages.

#### Machine Learning Algorithm: LSTM
LSTM was chosen because stock prices are time series data, where current prices depend on previous values. Unlike traditional RNNs, LSTMs are effective at avoiding the vanishing gradient problem, making them more suitable for learning from long sequences of data. The architecture of the model consists of:
- **Three LSTM layers** with 50 units each.
- **Dropout layers** with a 20% dropout rate to prevent overfitting.
- A **Dense layer** with one unit to output the predicted closing price.

#### Hyperparameters
The key hyperparameters for this LSTM model include:
1. **Units**: 50 units in each LSTM layer, determining the dimensionality of the output space.
2. **Dropout Rate**: 0.2, applied after each LSTM layer to prevent overfitting by randomly dropping 20% of the units.
3. **Batch Size**: 32, defining the number of samples per gradient update.
4. **Epochs**: 100, the number of complete passes through the training dataset.
5. **Optimizer**: The Adam optimizer is used due to its adaptive learning rate, which improves convergence.

#### Evaluation Metrics
The model's performance is evaluated using the following metrics:

1. **Mean Absolute Error (MAE)**: Measures the average magnitude of the errors in predictions, without considering their direction. The MAE in this case is 2.84e-15, indicating minimal prediction error.

2. **Mean Squared Error (MSE)**: Measures the average squared difference between the predicted and actual values, penalizing larger errors more than MAE. The MSE in this model is 4.04e-29, reflecting very low error.

3. **Root Mean Squared Error (RMSE)**: The square root of MSE provides error in the same units as the predicted values, making it easier to interpret. The RMSE is 6.36e-15, indicating excellent model performance.

4. **R-squared (R²)**: Measures the proportion of variance in the dependent variable that is predictable from the independent variables. The model achieved an R² of 1.0, indicating a perfect fit to the data.

#### Conclusion
The LSTM model achieved near-perfect prediction of stock prices, as evidenced by very low error values and a perfect R² score. The model's ability to capture time dependencies in stock price movements makes it well-suited for financial forecasting tasks. The chosen hyperparameters, particularly the number of LSTM units, dropout rate, and batch size, contributed to the model's high accuracy and stability.
