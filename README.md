# Objective
The objective of this project is to design and implement a complete data pipeline and analytical model to extract actionable business insights from an e-commerce dataset including: -Transforming raw transactional data into a structured star schema, -Performing SQL-based analysis (joins, aggregations, window functions)
Enabling business intelligence reporting through Power BI.
# Dataset
-Source: Kaggle, -File: ecommerce_sales_dataset.csv, -Records: 10,000 transactions, -Features: 26 columns.
Data includes:
-Customer data (ID, segment, gender, region, country),
-Product hierarchy (category, sub-category, product),
-Sales metrics (revenue, cost, profit, margin),
-Order details (date, payment method, status),
-Logistics (shipping cost, method, delivery time).
# Tools & Technologies
-Python (Pandas, Data cleaning and transformation), -SQLite (Database creation and SQL queries), -SQL (Joins, aggregations, window functions), -Power BI (Data visualization and dashboarding), -Google Colab (Development environment).
# Workflow
1. Data Preparation : Loaded raw dataset into Python, Cleaned and standardized columns, Handled duplicates and ensured data consistency.
2. Data Modeling (Star Schema): Created structured tables: Customers (5,348 unique customers), Orders (10,000 orders), Products (9,916 unique products), Order_items (fact table), Shipping/ Ensured: Unique keys in dimension tables, Proper one-to-many relationships.
3. Database Implementation: Built relational database using SQLite, Loaded structured tables, Validated data integrity.
4. SQL Analysis: Performed advanced queries including: Revenue by country, Revenue & profit by category, Top-performing products, Top customers by spending, Monthly revenue trends, Ranking using window functions.
5. Visualization (Power BI): Built interactive dashboard, Implemented slicers (Country, Category, Year), Designed KPI cards and trend visuals.
# Key Results
-Revenue by Country (Top markets): USA ($483K), Mexico ($475K), Canada ($472K).
-Revenue by Category: Electronics dominates($3.38M) significantly higher than others, followed by Home & Kitchen ($892K) and Clothing ($407K).
-Top Customers: (Highest spender): Customer from Japan ($20K+), high-value customers distributed across multiple countries.
-Top Products: (Top product generated): ~$19.9K revenue, revenue distribution is relatively spread across products.
-Profit by Category (Electronics leads profitability): $925K profit, strong margin contribution across all categories.
-Time-Based Trends: Revenue shows strong growth from 2021 to 2023, peak performance: Late 2023 (Oct–Nov) , decline observed in 2024 (likely incomplete data).
# Key Insights
-Market Performance: North American countries dominate revenue, emerging markets (India, Egypt, Jordan) show strong potential. 
-Product Strategy: Electronics is the core revenue and profit driver, other categories contribute but at significantly lower scale.
-Customer Behavior: Revenue is not concentrated in a single customer, healthy distribution reduces dependency risk.
-Seasonality & Trends: Strong upward trend from 2021 to 2023, peak sales occur in Q4 (holiday season effect).
-Business Efficiency: High profit margins in Electronics suggest strong pricing strategy and ffficient cost management.
