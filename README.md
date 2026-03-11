# Retail-Sales-Data-Analysis-EDA-Project-(PYTHON)
Project Overview

This project performs Exploratory Data Analysis (EDA) on a retail sales dataset containing 50,000 transactions. The objective is to clean messy data, analyze sales patterns, and generate business insights that help improve marketing, sales strategy, and decision-making.

The project focuses on data cleaning, feature engineering, visualization, and business insight generation using Python.

Objectives

Clean messy retail transaction data
Handle missing values and inconsistencies
Perform exploratory data analysis
Identify key sales patterns
Generate actionable business insights
Visualize trends for better decision making
Dataset Description
The dataset contains 50K retail transactions with the following features:

Column	Description
order_id	Unique order identifier
order_date	Date of purchase
city	Customer city
category	Product category
quantity	Units purchased
unit_price	Price per unit
discount_percent	Discount applied
final_unit_price	Price after discount
revenue	Total order revenue
sales_channel	Online / In-store
payment_method	Payment type
customer_type	New / Returning
Project Workflow

1) Data Loading :-

Dataset imported using Pandas

import pandas as pd
df = pd.read_csv("retail_sales_50k_messy.csv")

2) Data Cleaning :-

Key cleaning steps performed:

Removed duplicate records
Standardized city names
Converted date columns to datetime
Handled missing values
Fixed incorrect price calculations

Example:

df['city'] = df['city'].str.title()
df['order_date'] = pd.to_datetime(df['order_date'])

3) Feature Engineering :-

New features created:
Month
Year
Revenue calculation
Discount impact

Example:

df['revenue'] = df['quantity'] * df['final_unit_price']

4) Exploratory Data Analysis :-

Analysis performed on:
Category Sales
Identify highest revenue generating categories.
City Performance
Find top performing cities.
Sales Channel Analysis
Compare online vs in-store sales.
Discount Impact
Understand effect of discount on revenue.

5) Data Visualization :-

Libraries used:
Matplotlib
Seaborn

Example visualization:
import seaborn as sns
import matplotlib.pyplot as plt

sns.barplot(x='category', y='revenue', data=df)
plt.show()

Visualizations created:

Category revenue distribution
Sales by city
Discount vs revenue
Sales channel comparison
Monthly sales trends

Business Insights
1. Fashion category generates highest revenue
This category shows strong demand and growth potential.

2. Top revenue cities
Kolkata
Delhi
Bengaluru
Pune
These markets should receive more marketing investment.

3. Online sales channel slightly outperforms in-store sales
Digital channels should be prioritized.

4. Heavy discounts do not significantly increase revenue
Discount strategy should be optimized.

5. Data quality issues detected
Missing financial values can impact reporting accuracy.

Technologies Used
Tool	Purpose
Python	Data analysis
Pandas	Data manipulation
NumPy	Numerical operations
Matplotlib	Visualization
Seaborn	Statistical charts
Jupyter Notebook	Analysis environment
Project Structure
Retail_EDA_Project
│
├── Retail_EDA.ipynb
├── retail_sales_50k_messy.csv
├── README.md

* Key Skills Demonstrated :- 

Data Cleaning
Exploratory Data Analysis
Data Visualization
Business Insight Generation
Python for Data Analysis

* Future Improvements :-

Build Power BI dashboard
Create predictive sales model
Implement automated data validation
Add customer segmentation analysis

Author

Shantanu Shete

Data Analytics | Python | SQL | Power BI | Machine Learning
