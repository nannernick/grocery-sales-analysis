# Grocery Sales Drivers: Corporación Favorita Store Sales Analysis

## Dashboard
In Progress

## Questions
What drives grocery sales (seasons, paydays, promotions, holidays), and which product catagories are most sensitive to each driver.

## Data 
- Source: [Kaggle "Store Sales - Time Series Forecasting"] (https://www.kaggle.com/competitions/store-sales-time-series-forecasting). 
- About 3 Million rows of data tracking sales across 54 stores and 33 product families between 2013 and 2017. 
- 4 Dates are missing from the data
- Promotion data starts in April of 2014, so promo analysis is from that period onward

## Method
- Loaded the CSVs from Kaggle into a SQLite database with pandas
- Joined and aggragated sales with SQL queries
- Analyzed seasonality, promotions, and holidays in Python (pandas)
- Built an interactive dashboard in Tableau Public

## Key Findings
In Progress

## Limitations
- The set did not contain any price or cost data, so it only tracks revenue, not profit or margin
- Promotions and paydays are associations, not proven causes
- This chain is a South American retailer, so results may not translate to US grocery markets

## Repo Structure
- "notebooks/" : testing and analysis notebooks
- "sql/" : SQL Queries
- "outputs/" : exported tables and dashboard screenshots