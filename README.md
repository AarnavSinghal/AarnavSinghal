# Stock Price Prediction using Machine Learning  
Capstone Project – IITG DS Course

This project builds a complete **end-to-end ML pipeline** to predict stock returns using historical NASDAQ data.  
The workflow includes data cleaning, feature engineering, model training, evaluation, and backtesting.

---

## Project Overview

The goal is to predict **next-day returns** for a chosen target stock (e.g., AAPL) using:

- Historical OHLCV data  
- Technical indicators  
- Market index (QQQ) for benchmarking  
- Machine learning models (Linear Regression, Random Forest, XGBoost, LSTM optional)

This notebook follows a structured multi-phase workflow.

---

## Project Structure

### **Phase 1: Data Loading & Cleaning**
- Loads raw per-ticker CSVs  
- Forward-fills missing values  
- Aligns all tickers on a unified date index  

### **Phase 2: Feature Engineering**
- Computes daily returns  
- Generates technical indicators:  
  - Moving Averages (5/10/20)  
  - RSI  
  - MACD  
  - Volatility features  
- Merges target & market proxy (QQQ)

### **Phase 3: Dataset Construction**
- Creates supervised ML labels (`next_day_return`)  
- Builds the feature matrix `X` and target vector `y`  
- Train/validation split with time-based methodology  

### **Phase 4: Model Training & Evaluation**
Models used:
- **Linear Regression**  
- **Random Forest Regressor**  
- **XGBoost Regressor**

Metrics:
- MAE  
- RMSE  
- Sign Accuracy (directional prediction)  

### **Phase 5: Backtesting**
- Simulates a simple long/short strategy  
- Uses predicted signs to generate trading signals  
- Calculates cumulative returns vs. buy-and-hold benchmark  

---

## Results Summary

- ML models achieve meaningful predictive accuracy  
- Direction-based prediction (sign accuracy) is the key metric  
- Backtesting demonstrates how the model would perform in real trading conditions  

*(You can fill in numbers here after running the final results.)*

---

## Dataset

Dataset used:  
**Stock Market Dataset (NASDAQ)**  
Source: Kaggle  
Contains: Daily OHLCV data for hundreds of tickers up to April 2020.

---

## Technologies & Libraries

- Python  
- NumPy / Pandas  
- scikit-learn  
- XGBoost  
- Matplotlib / Seaborn  
- Google Colab  
- GitHub  

---

## How to Run

1. Open the notebook in **Google Colab**  
2. Upload the dataset folder  
3. Run all cells sequentially  
4. Modify the target stock via the `TARGET` variable  

---

## Key Learnings

- Time-series preprocessing  
- Feature engineering for financial data  
- Avoiding data leakage  
- Model comparison  
- Backtesting strategies  

---

## License

This project is submitted as part of an academic capstone requirement.  
Feel free to fork and experiment — just credit the original repository.

---

## Author

**Aarnav Singhal**  
IIT Guwahati DS course
student code- iitg_ds_2501432

---



<!--
**AarnavSinghal/AarnavSinghal** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
