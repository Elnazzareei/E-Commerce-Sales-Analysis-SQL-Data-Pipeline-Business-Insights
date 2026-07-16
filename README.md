# Objective
Design and implement a full pipeline to extract actionable business insights from raw e-commerce transaction data:
Transform raw flat data into a structured star schema,
Perform SQL-based analysis (joins, aggregations, window functions),
Enable BI reporting through an interactive Power BI dashboard.
# Dataset
Source: Kaggle,
File: ecommerce_sales_dataset.csv,
Records: 10,000 transactions, 26 columns,
Includes: customer data (ID, segment, gender, region, country), product hierarchy (category, sub-category, product), sales metrics (revenue, cost, profit, margin), order details (date, payment method, status), and logistics (shipping cost, method, delivery time).
# Tools & Technologies
Python (Pandas) , SQLite , SQL (joins, aggregations, window functions) , Power BI , Google Colab.
# Workflow
1. Data Preparation : Loaded the raw dataset into Python, cleaned and standardized columns, checked for duplicates and consistency issues.
2. Data Modeling (Star Schema): Split the flat file into structured tables:
Customers — 5,348 unique customers,
Orders — 10,000 orders,
Products — 9,916 unique products,
Order_items — fact table (revenue, cost, profit, discount per line item),
Shipping — cost, method, delivery time per order.
Ensured unique keys on dimension tables and proper one-to-many relationships to the fact table.
3. Database Implementation: Built a relational database in SQLite, loaded all five tables via Pandas' to_sql(), and validated row counts and key uniqueness.
4. SQL Analysis: Wrote queries using joins, aggregations, and window functions to answer:
Revenue by country,
Revenue & profit by category,
Top-performing products,
Top customers by spending,
Monthly revenue trends,
Country ranking via RANK() OVER (...).
5. Visualization (Power BI): Built an interactive dashboard with slicers (Country, Category, Year), KPI cards, and trend visuals for revenue, profit, and shipping performance.
# Key Results
-Top markets by revenue: USA ($483K), Mexico ($475K), Canada ($472K).
-Revenue by category: Electronics dominates at $3.38M — well ahead of Home & Kitchen ($892K) and Clothing ($407K).
-Top customer: highest spender based in Japan (~$20K); high-value customers distributed across multiple countries rather than concentrated in one.
-Top product: best-selling product generated ~$19.9K in revenue, with the rest of revenue spread fairly evenly across the catalog.
-Profit by category: Electronics leads with $925K profit and the strongest margin contribution overall.
-Time-based trends: strong revenue growth from 2021–2023, peaking in Oct–Nov 2023; the apparent decline in 2024 is confirmed to be a data cutoff, not a real trend — the dataset ends December 24, 2024, so 2024 has  about 7 fewer days of data than the other full years.
# Key Insights
Market performance: North America dominates revenue, while emerging markets (India, Egypt, Jordan) show strong potential for growth.
Product strategy: Electronics is the core revenue and profit driver; other categories contribute meaningfully but at a smaller scale.
Customer behavior: revenue is well-distributed across customers rather than concentrated in a few accounts, reducing dependency risk.
Seasonality: clear Q4 / holiday-season peak, consistent with a 2021–2023 upward trend.
Business efficiency: Electronics' high margin suggests effective pricing and cost management relative to other categories.
