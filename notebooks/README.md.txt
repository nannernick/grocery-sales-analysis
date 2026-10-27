# Grocery Sales Drivers: Corporación Favorita Store Sales Analysis

## Dashboard
In Progress

## Questions
What drives grocery sales (seasons, paydays, promotions, holidays), and which product catagories are most sensitive to each driver?

## Data 
- Source: [Kaggle "Store Sales - Time Series Forecasting"] (https://www.kaggle.com/competitions/store-sales-time-series-forecasting). 
- About 3 Million rows of data tracking sales across 54 stores and 33 product families between 2013 and 2017. 
- 4 Dates are missing from the data
- Promotion data starts in April of 2014, so promo analysis is from that period onward
- Produce is only populated in some months before June 2015, and nine product families first appear in January 2014, so year-over-year comparisons before 2016 aren't reliable.

## Method
- Loaded the CSVs from Kaggle into a SQLite database with pandas
- Joined and aggragated sales with SQL queries
- Analyzed seasonality, promotions, and holidays in Python (pandas)
- Built an interactive dashboard in Tableau Public

## Key Findings

**Seasonality and Monthly Timing**
- **Weekends:** Sales are about 42% higher on weekends than weekdays. Sunday is also the peak and Thursday is the low with Sundays being about 64% higher.
- **December:** Average daily sales in December are about 32% above a typical day for that year (2013-2016).
- **First week of the month:** Sales in the first 7 days of the month run about 13% above the rest, after comparing each day to the same weekday in the same month. A mid-month (15th) increase is not visible after controlling for weekday, month, and year.

**Category mix, promotions, holidays**
- **Concentration:** Grocery I, Beverages, and Produce made up 66.5% of 2016 sales.
- **Growth:** Comparing January-July 2017 to the same months in 2016 (the only window where every product family is fully populated in both years), unit sales rose about 10% overall. Beverages grew fastest among the major categories at about 17%, while Grocery I, the largest, grew about 9%.

## Limitations
- The set did not contain any price or cost data, so it only tracks unit sales, not profit or margin
- Promotions and paydays are associations, not proven causes
- This chain is a South American retailer, so results may not translate to US grocery markets
- "Sales" are unit counts, not revenue. Category growth includes one added store and a 2016 base that may be inflated by the April 2016 earthquake.

## Repo Structure
- "notebooks/" : testing and analysis notebooks
- "sql/" : SQL Queries
- "outputs/" : exported tables and dashboard screenshots