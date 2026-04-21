# Sales-Forecasting-Using-Time-Series-Models

 Overview:

This project builds an end-to-end sales forecasting system using advanced time series techniques on retail store data. The goal is to accurately predict daily sales by capturing seasonality, promotions, and customer behavior.

Three models were implemented and compared:

ARIMA (statistical baseline)
Prophet (interpretable forecasting)
LSTM (deep learning)

 Objective:
 
Forecast daily store sales
Analyze the impact of promotions and holidays
Compare classical vs machine learning vs deep learning approaches
Deliver business-ready insights

 Dataset:
 
Rossmann Store Sales dataset (Kaggle)
Data includes:
Sales, Customers
Promotions (Promo, Promo2)
Holidays (StateHoliday, SchoolHoliday)
Store information (Competition, Assortment, StoreType)

 Data Preparation:
 
Handled missing values (competition, promo intervals, store metadata)
Converted date columns to datetime format
Merged store and sales datasets
Filtered and structured data for time series modeling
Ensured consistent indexing and alignment across models

 Exploratory Data Analysis (EDA)

Key insights:

 Strong weekly and yearly seasonality
 Promotions significantly increase sales
 Holidays create noticeable spikes/drops
 Sales patterns vary across stores
 Feature Engineering
 
Extracted time-based features:
Day, Month, Year
Day of Week
Created lag features for temporal learning (LSTM)

Incorporated external drivers:
Promotions
Customers
Competition distance
Added holiday indicators for enhanced forecasting
 Models Implemented
 
 ARIMA
Baseline statistical model
Captures linear trends and seasonality

 Prophet
Handles trend and seasonality decomposition
Enhanced with:
Holiday effects
External regressors (Promo, Customers, Competition)
Hyperparameter tuning

 LSTM
Deep learning model for sequence prediction
Captures nonlinear patterns and temporal dependencies
Uses scaled sequences and sliding window approach

 Model Performance:
Model	  RMSE	  MAE	  MAPE
ARIMA	  983	    830	  20.93%
Prophet	126,785	109,860	1818%
LSTM	  793	    656	  14.89%

 Best Model: LSTM

 Visualization

The project includes:

Actual vs Predicted comparison plots
Zoomed-in forecasts (last 100 days)
Error comparison (Prophet vs LSTM)

Prophet trend & seasonality components
 
 Key Insights:
 Promotions Drive Sales
Significant spikes observed during promotional periods
Strong feature for predictive modeling

 Seasonality Matters
Weekly and holiday patterns strongly influence sales

 Store-Level Variation
Each store behaves differently → global models underperform

 LSTM Captures Complexity
Outperforms ARIMA and Prophet
Handles nonlinear and sudden changes effectively

 Challenges & Learnings:
 Handling multiple time series required store-level modeling
Initial LSTM scaling issues caused unrealistic predictions
Time index misalignment led to incorrect evaluations
Fixing these improved model accuracy significantly

 Conclusion:
LSTM is the most effective model for this problem
Traditional models provide useful baselines but lack flexibility
Incorporating business features (promo, holidays) improves forecasting
Proper preprocessing and alignment are critical for reliable results

 Recommendation:
Deploy LSTM-based forecasting for real-world retail scenarios, supported by interpretable models like Prophet.

 Tech Stack:
Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Statsmodels (ARIMA)
Prophet
TensorFlow / Keras (LSTM)

 Author:

Chibueze S. Imediegwu
Data Scientist | Machine Learning Engineer
