📈 S&P 500 Stock Prediction using Machine Learning

This project focuses on predicting the next-day movement of the S&P 500 index using historical stock data and machine learning techniques. It uses a Random Forest Classifier along with feature engineering and backtesting to evaluate performance.

🚀 Project Overview
Data is fetched using the yfinance API
Goal: Predict whether the market will go UP (1) or DOWN (0) the next day
Uses historical trends and engineered features
Evaluates performance using precision score
Implements backtesting for realistic evaluation
📊 Dataset
Source: Yahoo Finance via yfinance
Index: S&P 500 (^GSPC)
Time Period: 1927 – 2025
Features:
Open
High
Low
Close
Volume
🛠️ Tech Stack
Python 🐍
Pandas & NumPy
Matplotlib
Scikit-learn
yFinance API
⚙️ Workflow
1. Data Collection
Pulled historical S&P 500 data using yfinance
2. Data Preprocessing
Removed unnecessary columns (Dividends, Stock Splits)
Created a Target variable:
1 → Price goes up next day
0 → Price goes down
<img width="721" height="125" alt="visual selection" src="https://github.com/user-attachments/assets/527a7aeb-1a4c-4d15-ada5-db43a71ab53f" />


4. Feature Engineering
Created new features:
Rolling averages
Trend indicators
Ratio features across multiple horizons:
2 days
5 days
60 days
250 days
1000 days
5. Model Building
Used Random Forest Classifier
Tuned parameters:
n_estimators
min_samples_split
Probability threshold (0.6)
6. Backtesting
Implemented a custom backtesting function:
Train on past data
Test on future data in steps
Simulates real-world prediction scenario
📈 Results
Model Stage	Precision Score
Basic Model	1.00
Backtesting Model	~0.53
Improved Model	~0.56
Final model shows realistic performance after backtesting
Avoids overfitting seen in initial model
🧠 Key Learnings
Backtesting is crucial for time-series models
Feature engineering significantly improves performance
Financial markets are noisy → perfect accuracy is unrealistic
Precision is more useful than accuracy in trading problems
📦 Installation
pip install yfinance pandas numpy matplotlib scikit-learn
▶️ How to Run
python your_script_name.py

Or run in Jupyter Notebook.

📌 Future Improvements
Add more indicators (RSI, MACD)
Try advanced models (XGBoost, LSTM)
Hyperparameter tuning
Use sentiment analysis (news data)
📎 Project Structure
├── data/
├── notebook.ipynb
├── model.py
├── README.md
🙌 Author

Bhavna Meena
