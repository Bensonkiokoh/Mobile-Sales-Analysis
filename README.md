# Mobile-Sales-Analysis

## Table Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Dataset Overview](#dataset-overview)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)

### Project Overview
This project explores mobile phone sales data from a major retailer to uncover patterns in product performance, customer behavior, and regional trends. The dataset includes transaction records, customer demographics, product details, and sales channels across multiple countries.
Using Power BI & Power Query the analysis focuses on answering key business questions such as:

-	Which mobile brands and models are the top sellers overall and in specific countries or cities?
-	How do sales numbers vary by storage size, color, or operating system (Android vs. iOS)?
-	What is the typical customer profile - age group, gender - for different brands or models?
-	How do sales and revenues break down across different sales channels (online, partner, in-store) and payment types?
-	Are there noticeable differences in pricing and sales volume between regions or cities?
-	Which countries or cities generate the highest total revenue and units sold?
-	Are there patterns in customer demographics based on mobile brand, model, or price range?
-	How does sales performance change month over month in 2024?
-	Are there correlations between customer age groups and the type of devices they purchase (for example, younger customers preferring certain brands)?
### Data Source 
This project is based on a dataset provided in the May 2025 DataDNA Challenge by Onyx Data. The data simulates mobile phone sales across multiple regions and includes transactions, customer demographics, product specs, and sales channels.
### Dataset Overview
- Source: Onyx Data (DataDNA Challenge)
- Date: May 2025
- Format: Excel (.xlsx)
#### Contents:
- Sales transactions (order date, quantity, price, region)
- Customer details (age, gender, location)
- Product information (model, brand, category)
- Sales channels (retail, online, distributor)

The dataset is intended for analytical exploration, dashboard building, and data storytelling.

### Tools Used
- Power BI – for creating interactive dashboards and reports
- Power Query (M) – for cleaning, shaping, and transforming the raw data
- DAX – for calculated columns, KPIs, and advanced metrics
  
These tools were used to turn raw sales records into meaningful insights for business decision-making.
### Data Cleaning & Preparation
1. Removed empty columns and dropped irrelevant fields not needed for analysis
2. Corrected data types for each column (dates, numbers, text, etc.)
3. Created a calendar table for time-based analysis (with Year, Month, Quarter columns)
4. Renamed columns for clarity and consistency
5. Removed duplicate entries in sales or customer records
6. Added calculated columns:
   - Total Sales = Quantity * Unit Price
   - Extracted Year, Month, Week, etc. from the order date
### Exploratory Data Analysis (EDA)
The goal of EDA was to explore the dataset, uncover early patterns, and surface any data quality issues before building the dashboard.
#### What I Explored:
- Sales Distribution
  - Analyzed total sales by product, region, and sales channel
  - Identified top-selling models and low performers
- Time Trends
  - Tracked sales across months and quarters
  - Spotted seasonal spikes and slow periods
  - Observed growth/decline patterns over time
- Customer Demographics
  - Explored sales by gender and age group
  - Found demographic differences across regions
  - Linked certain customer segments to specific brands or models
- Geographic Performance
  - Compared sales volume and revenue by region
  - Highlighted top-performing and underperforming areas
  - Spotted opportunities in low-sales regions
- Data Quality Checks
  - Checked for missing values, outliers, and invalid types
  - Found and handled extreme values in quantity and price
  - Verified data integrity across merged tables

### Data Analysis
After cleaning and exploring the data, I used Power BI and DAX to perform deeper analysis focused on identifying trends, patterns, and business opportunities.

- Identified top-selling mobile phone models by revenue and quantity
- Analyzed category-level performance (e.g., premium vs. budget phones)
- Tracked monthly and quarterly sales trends to uncover seasonality
- Compared sales across countries and regions to identify high- and low-performing markets
- Assessed regional product preferences to guide targeted marketing
- Highlighted the most valuable customer groups in terms of purchase frequency and revenue
- Identified which channels drive the most revenue, volume, and repeat customers
- Measured performance across different sales channels (online, retail, distributor
####  DAX Measures Used
- Sales Growth % (Month over Month)
```MoM Growth % = 
DIVIDE(
  [Total Sales] - CALCULATE([Total Sales], PREVIOUSMONTH('Date'[Date])),
  CALCULATE([Total Sales], PREVIOUSMONTH('Date'[Date]))
)
```
- Total Quantity Sold
``` Total Quantity = SUM('Sales'[Quantity])```
- Total Sales
```Total Sales = SUM('Sales'[Quantity] * 'Sales'[Unit Price])```

### Results & Findings
- Top 5 mobile models generated over 40% of total revenue, showing a strong reliance on a few key products
- Premium phones led in revenue, while budget phones dominated in units sold — suggesting different value drivers across segments
- Customers aged 25–34 drove the highest revenue; repeat purchases were most common among the 35–44 age group

### Recomendations
Based on the findings, here are data-backed recommendations for improving sales performance and business strategy:

- Invest in top-performing models through targeted promotions and inventory priority — they already generate over 40% of revenue.
- Expand mid-range offerings, especially those preferred by female and younger buyers, to capture a broader audience.
- Monitor low-sales months (April & June) for possible stock issues, weak campaigns, or regional holidays affecting demand.
- Leverage the weekend traffic with time-limited offers or flash sales to maximize conversion during peak buying days.
- Tailor product bundles or loyalty offers for customers aged 35–44 to encourage repeat purchases from an already-engaged segment.

### Limitations
While the analysis provided valuable insights, a few limitations should be considered:

- No Inventory or Stock Levels: It's unclear whether low sales in certain regions or months were due to demand or supply constraints.
- No External Benchmarks: The analysis didn’t include market data or competitor benchmarks to contextualize performance.
- Distributor Channel Detail: Lack of granular data in the distributor channel made it hard to diagnose performance issues.
- Limited Time Range: The dataset covers a single year (or partial year), making it hard to assess long-term trends or growth.

### References
- Dataset Source: Onyx Data - DataDNA Challenge (May 2025)
- Power BI: Microsoft Power BI Documentation
- Power Query M Language: Microsoft Power Query M Reference
- DAX Functions: DAX Guide by SQLBI
- Data Visualization Best Practices: Storytelling with Data
- Exploratory Data Analysis: Practical Statistics for Data Scientists















