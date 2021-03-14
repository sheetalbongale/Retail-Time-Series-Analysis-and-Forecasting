# Online Retail Sales Time Series Analysis Forecasting

![image](img/ts4.jpg)
## Challenge

The store is interested in maintaining the right inventory given its historical sales.
Build a model that predicts sales quantities for the 7 days from 11/27/2011 -
12/3/2011 Sun - Sat. To help the company prepare for the worst case, please
focus your predictions and the evaluation of your model on only the top three
selling items.

1. Include any exploratory data analysis and evaluations that support your
findings.
2. Please give us your estimated number of sales for these three items,
broken out by country.
3. Please briefly discuss why you chose your approach, its strengths and
drawbacks, and how you might approach this problem if you were to
research it further.

We define top selling items as items which had the greatest total sales over this
week across all countries.

## Data Overview
This is a public, transnational data set on transactions from
12/01/2010 and 12/09/2011 for a UK-based and registered non-store online retail
company.

**Columns:**
```
- InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned
to each transaction. If this code starts with letter 'c', it indicates a cancellation.
- StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely
assigned to each distinct product.
- Description: Product (item) name. Nominal.
- Quantity: The quantities of each product (item) per transaction. Numeric.
- InvoiceDate: Invice Date and time. Numeric, the day and time when each
transaction was generated.
- UnitPrice: Unit price. Numeric, Product price per unit in sterling.
- CustomerID: Customer number. Nominal, a 5-digit integral number uniquely
assigned to each customer.
- Country: Country name. Nominal, the name of the country where each customer
resides.
```

Source: http://archive.ics.uci.edu/ml/machine-learning-databases/00352/

## Steps

1. Data Wrangling and Exploratory Data Analysis
2. Feature Engineering and Selection
3. Modeling and forecasting
4. Model evaluation and validation
5. Sales quantity forecast results
6. Observation and analysis report

## Models under evaluation
- ARIMA
- SARIMA
- Prophet
- LSTM
