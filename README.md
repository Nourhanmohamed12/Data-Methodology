🛒 Walmart Sales Analysis Project
This project analyzes historical Walmart sales data from 45 stores across different regions to uncover insights about:

🏪 Store performance
🎉 Holiday impacts
🌸 Seasonal and monthly trends
📉 Economic factors

Goal: Understand how holidays, seasons, and economic indicators influence weekly sales and provide actionable recommendations to improve store revenue.

Dataset: Weekly sales data for 2010–2012 with store info, holiday flags, temperature, fuel price, CPI, and unemployment.

📂 Dataset

Source: Kaggle

Key Columns:

Column Name	Description
🏪 Store	Store number (1–45)
📅 Date	Week-ending date
💵 Weekly_Sales	Weekly sales in USD
🎉 Holiday_Flag	1 if holiday week, 0 otherwise
🌡 Temperature	Regional temperature
⛽ Fuel_Price	Fuel price in USD
📈 CPI	Consumer Price Index
📉 Unemployment	Regional unemployment rate
🏷 Type	Store type (A = Large, B = Medium, C = Small)

Additional Computed Columns:

Day, Month, Year, Season
Store_Type (Large, Medium, Small)
Sales_Category (High vs Low weekly sales)
Adjusted_Sales (Weekly sales adjusted by CPI)
🛠 Tools & Libraries
Python 3
Pandas, NumPy – Data manipulation
Matplotlib, Seaborn – Visualizations
Datetime – Date operations
warnings – Manage warnings
🧹 Data Cleaning & Preprocessing
✅ Checked for missing values & duplicates
✅ Converted Date column to datetime format
✅ Extracted day, month, year, and season
✅ Created additional columns: Store_Type, Sales_Category, Adjusted_Sales
✅ Handled outliers using IQR method for Weekly_Sales & Unemployment
✅ Filled missing values in Fuel_Price & Unemployment using mean/median
📊 Key Analyses & Insights
1️⃣ Store Performance
🏆 Store 20 → highest total weekly sales (strongest revenue)
⚡ Store 14 → highest variability in sales (most volatile)
📌 Store performance has stronger influence than macroeconomic indicators
2️⃣ Holiday Impact
Non-holiday weeks → higher total sales overall
🎉 Top holiday sales: Thanksgiving > Super Bowl > Labour Day > Christmas
Some stores (30, 36, 37, 38, 44) → negative impact from holiday weeks
3️⃣ Seasonal & Monthly Trends
🌸 April (Month 4) → highest total weekly sales
🌼 Spring → highest seasonal sales
📈 Seasonal/monthly patterns → optimal periods for promotions
4️⃣ Economic Factors Impact
⛽ Fuel Price & 📉 Unemployment → negatively correlated with sales
CPI → weak negative impact
Stores 12, 28, 38 → high fuel & unemployment → lower sales
5️⃣ Correlation Analysis
Strong positive correlation: Fuel_Price vs Year (fuel prices increased over time)
Weak/moderate negative correlation: economic indicators vs weekly sales
Store IDs & holiday-created columns excluded from correlation interpretation
📊 Visualizations
📊 Bar Charts → total weekly sales per store, month, season
🥧 Pie Charts → sales by holiday flag & season
📦 Boxplots & Histograms → distribution of sales, CPI, unemployment, temperature
🔹 Scatter Plots → sales vs economic indicators
💥 Bubble Chart → sales by season & holiday flag
🌡 Heatmap → correlation between numeric factors & weekly sales
💡 Key Recommendations
🌸 Focus promotions during April & Spring (peak season)
🎉 Encourage purchases during holidays with holiday flags
🎯 Target stores with high unemployment & fuel price for special offers
🦃 Thanksgiving → highest revenue, followed by Super Bowl & Labour Day
💾 Output & Export
💾 Cleaned dataset → walmart_clean.csv
📊 Heatmaps & charts → saved as PNG for reporting
📈 Additional computed columns → added to dataset
⚡ Usage
Clone the repository
Install required libraries:
pip install pandas numpy matplotlib seaborn
Run the Jupyter Notebook (.ipynb)
→ Reproduce analyses, visualizations, and cleaned datasets
🏁 Project Summary

This analysis provides a comprehensive view of Walmart store sales:

Top-performing stores 🏆
Seasonal trends 🌸
Holiday effects 🎉
Economic factor impacts 📉

Outcome: Insights can guide strategic promotions, resource allocation, and revenue maximization across stores.
