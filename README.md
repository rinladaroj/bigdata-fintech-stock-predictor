# bigdata-fintech-stock-predictor
# 📈 Data-Driven Market Intelligence: Enhancing Predictive Accuracy in Financial Markets through Hybrid Sentiment-Technical Analytics

## 🎯 Project Overview
This repository contains the final project for the **Big Data-Driven Business Analytics and Application** course. The project aims to predict stock price movements for leading technology companies (**Apple, Google, Tesla, Microsoft, and Amazon**) by building a hybrid machine learning model that merges quantitative financial time-series data with qualitative, sentiment-driven social media data (Twitter).

---

## 🏗️ System Architecture & Data Pipeline
1. **Data Cleaning & Feature Engineering:**
   - **Impactful Sentiment:** Weighted raw sentiment scores using social engagement metrics (Likes, Retweets, Comments) to measure true "market influence".
   - **Trend Filtering:** Integrated a 5-day Moving Average (`ma_5d`) as a baseline trend context.
   - **Market Context:** Included S&P 500 closing prices (`sp500_close`) to isolate stock-specific signals from systemic market movements.
2. **Database Modeling:** Designed a relational database schema (ER Diagram) to handle multi-source data integration cleanly, ensuring traceable data provenance from raw entries to the final dataset (`my_fintech_data.csv`).

---

## 🤖 Methodology & Model Performance
- **Benchmarking:** Screened multiple algorithms using `LazyPredict` and selected **XGBoost Classifier** as the core predictive engine for its robust handling of financial datasets and regularization.
- **Handling Imbalance & Validation:** Applied **SMOTE** (Synthetic Minority Over-sampling Technique) to address class imbalance and **TimeSeriesSplit** to prevent data leakage during temporal cross-validation.
- **Forecasting Horizons:** Evaluated performance across short-term ($t+1$) and medium-term ($t+7$) horizons, demonstrating strong persistence in market trend detection.

---

## 📊 Backtesting & Results
- Built an event-driven backtesting framework simulating a trading environment with transaction costs (0.1%) and disciplined position sizing (10% capital per trade).
- Over a 5-year test horizon, the sentiment-integrated strategy achieved a consistent upward equity curve, generating nearly a **100% total return** (Alpha generation).

---

## 🛠️ Tech Stack
- **Languages:** Python, SQL
- **Libraries:** XGBoost, Scikit-Learn, Pandas, NumPy, Matplotlib, Imbalanced-Learn (SMOTE), LazyPredict, YFinance
