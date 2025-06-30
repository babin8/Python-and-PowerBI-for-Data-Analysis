# Store Data Analysis

This project uses the daily sales data from a convenince store/smoke shop and analyzes the data for store performance insights.

**Tools Used**
- Jupyter Notebook
- Python (Pandas, matplotlib)

**Method**

1. Data Preparation

- Loaded the dataset using pandas.

- Cleaned and transformed columns: converted Date to datetime, removed $ symbols from numeric columns, and standardized column names for clarity.

- Sorted records chronologically for time-series accuracy.

2. Time-Based Aggregation

- Extracted Year, Month, and Week from each Date.

- Calculated weekly, monthly, and yearly average sales for smoother trend insights and comparisons.

3. Visual Analytics

- Line charts showing total sales trends by day of week, day of month, week, month, and year.
- Boxplots showing data distribution to detect outliers for the same trends.
- Color-coded the charts to differentiate high sales, medium sales, and low sales periods.

**Insights**

1. Overall Sales Trends

- Yearly Trend: Year-over-year growth appears modest and consistent, with some years showing stronger peaks.

- Monthly Trend: Certain months (like August and November/December) tend to have higher average sales, likely due to back-to-school and holiday shopping.

- Weekly Trend: This is the most volatile metric. Peaks and dips are clearly visible, influenced by both operational and seasonal factors.

2. Strongest vs Weakest Time Periods

Strongest Sales Periods

- Week 33 and Week 35 (mid-August): Consistent high average sales.

- Weeks 47–52 (late November through December): High-performing weeks, likely due to holiday season traffic. Weekends generally show higher average sales compared to weekdays.

Weakest Sales Periods

- Weeks 1–10 (early year, January–March): Low sales averages with low volatility, possibly post-holiday slowdowns or reduced seasonal demand.

- Some mid-year lows also appear around weeks 20–25, suggesting soft spots in customer engagement.

3. Weekly Grouping & Categorization

Using quantile-based segmentation:

- High Sales Weeks (top 25%) occur mostly in August and December.

- Medium Sales Weeks are evenly distributed across the year.

- Low Sales Weeks (bottom 25%) concentrate in early Q1 and some summer weeks.

4. Weekly Patterns Across Years
- Line graphs show strong repetition of patterns each year.

- Most outliers, both high and low, are isolated to specific dates and not part of sustained trends.

- Some years outperform others in specific weeks — likely due to marketing strategies, external factors, or business cycles.
