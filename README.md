# 📈 Stock Market Price Prediction using LSTM

A time series analysis project that uses Long Short-Term Memory (LSTM) neural networks to forecast the BSE Sensex stock index based on historical data from 1997 to 2024.

---

## 📚 Abstract

Predicting stock prices is challenging due to their dynamic and volatile nature. This project explores the use of LSTM (a type of Recurrent Neural Network (RNN)) for capturing long-term patterns in time-series financial data. The model was trained using Sensex weekly closing prices and achieved high accuracy in identifying trends and making predictions.

---

## 🧠 Model Overview

- **4× LSTM layers** for capturing sequential patterns
- **2× Dense layers** for feature abstraction
- **1× Dense output layer** for price prediction
- **Activation function**: ReLU
- **Optimizer**: Adam
- **Loss function**: Mean Squared Error (MSE)

---

## 🔧 Methodology

### 📊 Data Source
- **Dataset**: Historical weekly closing prices of BSE Sensex (1997–2024)
- **Source**: Yahoo Finance

### 🔄 Data Preprocessing
- Min-Max normalization
- Cubic Spline Interpolation to increase data points (from 22 to 1109)
- Train/Validation/Test Split: 80% / 10% / 10%
- Feature used: Weekly closing price only

### ⚙️ Hyperparameters
- Learning rate: `0.001`
- Batch size: `32`
- Epochs: `200`
- Early stopping with patience: `20 epochs`
- Learning rate decay factor: `0.5` (min: `1e-4`)

---

## 📈 Results

| Metric             | Value        |
|--------------------|--------------|
| Training MSE       | 7.477e-05    |
| Validation MSE     | 0.000313     |
| Test MSE           | 0.000247     |
| Test MAE           | 0.0059       |

### 📊 Visualizations
- Training vs Validation Loss Curve
- Actual vs Predicted Stock Prices

---

## ✅ Key Insights

- LSTM effectively captured long-term price trends
- Performance surpassed traditional methods like moving averages or linear regression
- Challenges in predicting sudden, news-driven market shocks

---

## ⚠️ Limitations

- Struggles with sharp market fluctuations caused by unseen external factors
- Computationally intensive for real-time prediction
- Sensitive to hyperparameters — tuning is crucial

---

## 🔮 Future Work

- Combine LSTM with traditional models for hybrid predictions
- Integrate news sentiment analysis to improve forecasting during volatile events

---

## 📄 License

This project is academic and intended for educational use only.
