# Restaurant Sales Forecasting

## Project Overview

This project develops a machine learning system to forecast **restaurant daily sales** using historical transaction data.

Unlike projects based on public benchmark datasets, this project uses a **real-world dataset collected from an actual restaurant**.

The goal is to use historical sales patterns to predict future restaurant sales and support better business planning.

## Real-World Dataset

The transaction data was collected directly from the restaurant.

The original dataset contained **22,896 transactions** with the following information:

* Date
* Time
* Item
* Unit Price
* Total Sales

After data cleaning and removing test transactions, **22,820 transactions** remained.

The cleaned data covered **60 days of restaurant sales**.

## Data Preprocessing

The data was cleaned and prepared through several steps:

* Checked missing values
* Checked duplicate records
* Identified and removed test transactions
* Converted dates into useful time features
* Aggregated transactions into daily sales
* Created lag features
* Created rolling statistical features
* Selected relevant features for modeling

## Features

The final model used features such as:

* Day index
* Day of week
* Weekend indicator
* Sine/cosine day-of-week features
* Previous-day sales
* 7-day lag sales
* 14-day lag sales
* 21-day lag sales
* 3-day rolling mean
* 7-day rolling mean
* 14-day rolling mean

## Forecasting Models

Two machine learning models were used:

### Linear Regression

Linear Regression was used as a baseline model for predicting daily restaurant sales.

### Random Forest

Random Forest was used to capture more complex relationships between historical sales patterns and future sales.

## Forecasting Tasks

The project was designed to investigate restaurant sales forecasting at different future horizons:

* Next 1 day
* Next 7 days
* Next 30 days

## Evaluation Metrics

The models were evaluated using:

* MAE — Mean Absolute Error
* RMSE — Root Mean Squared Error
* R² — Coefficient of Determination
* MAPE — Mean Absolute Percentage Error
* Accuracy within ±10%
* Accuracy within ±20%
* Accuracy within ±30%

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## Project Structure


restaurant-sales-forecasting/
│
├── notebooks/
│   └── restaurant_sales_forecasting.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore


## Business Value

Sales forecasting can help a restaurant with:

* Inventory planning
* Staff scheduling
* Purchasing decisions
* Financial planning
* Understanding sales patterns
* Preparing for expected changes in demand

## Limitations

The dataset covers a relatively short period of time, so longer-term forecasting can be difficult.

Future improvements could include collecting more months of transaction data and incorporating additional information such as holidays, promotions, weather, and special events.
