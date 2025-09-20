# Customer Segmentation Using RFM Analysis

## Project Overview
This project aims to analyze customer behavior and classify customers into three segments (High, Mid, Low) based on their purchase history using three key metrics: Recency, Frequency, and Monetary Value (RFM). The purpose is to enable targeted marketing and optimized customer retention strategies by understanding different customer groups through transactional data.

## Data Description
The `online retail` dataset contains the following columns:
- `InvoiceNo`: Invoice Number.
- `StockCode`: Stock code of the item sold.
- `Description`: Description on the item sold.
- `Quantity`: Quantity of the item sold.
- `InvoiceDate`: Date on which the invoice was sent.
- `UnitPrice`: Price per unit of quantity.
- `CustomerID`: Unique ID of the customer.
- `Country`: Country of origin of the customer.

## Prerequisites
- Python 3.x
- Libraries: `pandas`, `plotly`
- Jupyter Notebook for interactive execution

## Exploratory Data Analysis (EDA)
- **Shape**: 541909 rows, 8 columns.

- **Data Types** : 
   - Numerical: Quantity (int64), UnitPrice (float64), CustomerID (float64)
   - Categorical: InvoiceNo , StockCode , Description , InvoiceDate , Country

- **Missing Values** :
   - `Customer ID` : 24%
   - `Description` : 0.2 %

## Data Cleaning
- `Customer ID` : Drop Nulls

## Data Transformation : 
- `InvoiceDate` : Change data type to date
- `Total Amount` : create new column that equal total amount = UnitPrice*Quantity

## Key Findings and Insights
### KPIs:
- Number of Unique Customers : 4372
- Number of Unique Products : 3684
- Number of Unique Invoices : 22190
- Number of Countries : 37
- Total Revenue : 8300065
- Total Quantity Sold : 4906888
- Average Sales Amount per Transaction : 20.40
- Average Quantity Sold per Transaction : 12.06
- Average Revenue per Customer : 1898.45
- Average Revenue per Order : 374.04

### Analysis and Visualizations
- Top 5 countries nased on number of customers (US , Germany , France , EIRE , Spain)
- Top 3 Countries by Revenue (US , Netherlands , EIRE)
- Top 3 Countries by Orders (US , Germany , France)
- Top Product by Revenue : `Regency Cakestand 3 Tier`
- Top Product by Orders : `World War 2 Gliders Asstd Designs`

## RFM Model:
   - The RFM model was built for each customer:
      - Recency: Days since last purchase.
      - Frequency: Number of purchases.
      - Monetary Value: Total spend.

   - Customers received scores (1-4) for each metric based on quartiles, with composite “RFM Score” used for segmentation.

   - Customers were categorized:
   -  High Level (Score 10-12)
   -  Mid Level (Score 6-9)
   -  Low Level (Score 3-5)

   ### Segmentation Results :
   - Midlevel : 1,899	(Moderate loyalty/value)
   - Highlevel : 1,690	(Best, most loyal/high value)
   - Lowlevel : 783	(Least engaged, at risk)

## Recommendations:
- Prioritize retention strategies (special offers, loyalty programs) for high-level customers, who drive the bulk of revenue.

- Develop win-back campaigns and personalized messaging for low-level and at-risk customers.