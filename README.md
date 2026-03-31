Walmart Sales Analysis Project
Project Overview

This project analyzes historical Walmart sales data from 45 stores across different regions to uncover insights about sales patterns, store performance, holiday impacts, and economic factors. The main goal is to understand how holidays, seasons, and economic indicators influence weekly sales, and to provide actionable recommendations to improve store revenue.

The dataset contains weekly sales data for 2010–2012 and includes store information, holiday flags, temperature, fuel price, CPI, and unemployment.

Dataset

The dataset used in this project was obtained from Kaggle and contains the following key columns:

Column Name	Description
Store	Store number (1–45)
Date	Week-ending date
Weekly_Sales	Weekly sales in USD
Holiday_Flag	1 if the week is a special holiday week, 0 otherwise
Temperature	Temperature in the region
Fuel_Price	Fuel price in USD
CPI	Consumer Price Index
Unemployment	Unemployment rate in the region
Type	Store type (A = Large, B = Medium, C = Small)

Additional computed columns include Day, Month, Year, Season, Store_Type, Sales_Category, and Adjusted_Sales.

Tools & Libraries
Python 3
Pandas, NumPy
Matplotlib, Seaborn
Datetime
Warnings management (warnings module)
Data Cleaning & Preprocessing
Checked for missing values and duplicate rows (dataset is initially clean).
Converted Date column to datetime format.
Extracted day, month, year, and season from Date.
Created additional columns for analysis:
Store_Type (Large, Medium, Small)
Sales_Category (High vs Low weekly sales)
Adjusted_Sales (Weekly sales adjusted by CPI)
Handled outliers using the IQR method for Weekly_Sales and Unemployment.
Filled missing values in Fuel_Price and Unemployment using mean/median.
Key Analyses & Insights
1. Store Performance
Store 20 had the highest total weekly sales → strongest revenue performer.
Store 14 had the highest variability in sales → most volatile store.
Store performance has a stronger influence on sales than macroeconomic indicators.
2. Holiday Impact
Non-holiday weeks generated higher total sales overall.
Among holidays, Thanksgiving produced the highest average sales, followed by Super Bowl, Labour Day, and Christmas.
Some stores (e.g., 30, 36, 37, 38, 44) showed negative impacts from holiday weeks.
3. Seasonal & Monthly Trends
April (Month 4) recorded the highest total weekly sales.
Spring season had the highest sales overall.
Seasonal and monthly patterns suggest optimal periods to run promotions.
4. Economic Factors Impact
Fuel Price and Unemployment negatively correlated with weekly sales.
High fuel prices → lower sales.
High unemployment → lower sales.
CPI had a weak negative impact.
Stores 12, 28, 38 have high unemployment and fuel prices, resulting in lower weekly sales.
5. Correlation Analysis
Strong positive correlation between Fuel_Price and Year → fuel prices increased over time.
Weak to moderate negative correlation between economic indicators (Fuel_Price, CPI, Unemployment) and weekly sales.
Store IDs and holiday-created columns were excluded from meaningful correlation interpretation.
Visualizations
Bar Charts: Total weekly sales per store, per month, per season.
Pie Charts: Total sales by holiday flag and season.
Boxplots & Histograms: Distribution of weekly sales, CPI, unemployment, and temperature.
Scatter Plots: Weekly sales vs economic indicators to visualize relationships.
Bubble Chart: Weekly sales by season and holiday flag.
Heatmap: Correlation between key numeric factors and weekly sales.
Key Recommendations
Focus promotions during April and Spring → peak sales season.
Encourage purchases during holidays by implementing holiday flags, especially in stores with lower weekly sales.
Target stores with high unemployment and fuel price for special offers to boost sales.
Thanksgiving promotions yield the highest revenue among holidays, followed by Super Bowl and Labour Day.
Output & Export
Cleaned dataset saved as walmart_clean.csv.
Heatmaps and charts saved as PNG files for reporting purposes.
Additional computed columns added to dataset for analysis.
Usage
Clone the repository.

Install required libraries:

pip install pandas numpy matplotlib seaborn
Run the Jupyter Notebook (.ipynb) to reproduce all analyses, visualizations, and cleaned datasets.
Project Summary

This analysis provides a comprehensive view of Walmart store sales, uncovering top-performing stores, seasonal trends, holiday effects, and the influence of economic factors. Insights can be used for strategic promotions, resource allocation, and revenue maximization across stores.
