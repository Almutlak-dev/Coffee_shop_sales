# Coffee_shop_sales
This project analyzes 149k+ coffee shop sales transactions from three store locations and provides an interactive Streamlit dashboard for data exploration and daily revenue prediction.

An end-to-end data analytics and machine learning project analyzing 149k+ coffee shop sales across three store locations, followed by building an interactive Streamlit dashboard and a Random Forest prediction model for daily revenue forecasting.

 Project Overview

This project focuses on:

Cleaning and preparing a large retail sales dataset

Performing exploratory data analysis (EDA) to identify business trends

Building interactive visualizations using Matplotlib and Plotly

Creating a Streamlit dashboard for real-time insights

Training a Random Forest Regression model to predict daily revenue

Deploying the dashboard online

  Project Structure
├── app.py                     # Streamlit dashboard
├── clean_coffee_sales.csv     # Cleaned dataset
├── daily_revenue_model.pkl    # Trained Random Forest model
├── README.md                  # Project documentation
├── requirements.txt           # Dependencies for deployment

1. Data Cleaning

Key cleaning steps:

Converted transaction_date and transaction_time into a merged datetime

Removed whitespace from column names

Extracted useful features: hour, day, month, day_of_week, is_weekend

Handled missing & incorrect values

Ensured numerical columns are correctly typed

2. Data Exploration

Explored:

Sales distribution by product type

Sales performance across store locations

Peak hours and peak days

Daily revenue trends over several months

3. Exploratory Data Analysis (EDA)

The EDA includes:

Bar charts for top-selling products

Line charts for hourly transactions

Store comparison charts

Daily revenue over time

Each visualization includes captions and insights describing observed patterns.

4. Machine Learning – Revenue Prediction

Model used: RandomForestRegressor

Features used

Day

Month

Year

Day of week

Weekend flag

Results

Random Forest produced the lowest RMSE (~360), outperforming Linear Regression.

The final model was saved as .pkl using pickle:

pickle.dump(rf, open("daily_revenue_model.pkl", "wb"))

 5. Streamlit Dashboard

The dashboard includes:

Sidebar filters (Store, Product Category, Date Range)

Dataset description

Summary statistics

Dynamic interactive charts

Revenue prediction tool

Key insights section

To run locally:

streamlit run app.py

Deployment

The app is deployed using Streamlit Cloud.

Add a proper requirements.txt:

streamlit
pandas
numpy
scikit-learn
matplotlib
plotly


Then link your GitHub repo → Streamlit Cloud → Deploy.

Key Insights

Coffee and tea products dominate overall transactions

Hell’s Kitchen and Astoria are the highest-performing stores

Peak hours occur around 9–10 AM

Revenue steadily increases month over month

Weekends show slightly higher average revenue

References

Streamlit Documentation: https://docs.streamlit.io

Pandas Documentation: https://pandas.pydata.org

Scikit-learn Documentation: https://scikit-learn.org

Matplotlib Documentation: https://matplotlib.org

Plotly Express Guide: https://plotly.com/python/plotly-express

👨‍💻 Author

Abdulwahab Almutlak
AI & Data Science Enthusiast
GitHub: almutlak-dev
