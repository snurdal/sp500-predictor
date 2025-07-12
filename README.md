# 📈 (S&P 500) Stock Market Prediction

This project uses historical data from the **S&P 500** index to predict whether the market will go up the next day.

### What does it do?

- Fetches full historical S&P 500 data using the `yfinance` API
- Creates new predictive features like:
  - Moving average ratios
  - Recent trend counts
- Trains a **Random Forest Classifier** to predict the next day’s movement
- Returns both actual and predicted values for validation

### 🛠️ Technologies

- Python
- pandas, yfinance
- scikit-learn (RandomForestClassifier)
- matplotlib (optional, for visualization)

### 📥 Data Source

All data is pulled directly from **Yahoo Finance** using `yfinance`:
```python
import yfinance as yf
sp500 = yf.Ticker("^GSPC").history(period="max")

