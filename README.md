# Consumer-Shopping-Behaviour-Analysis
Analyzed customer shopping behavior using Python (Pandas) for data cleaning and EDA, PostgreSQL for SQL-based analysis to identify revenue trends across age groups and product categories, and built an interactive Power BI dashboard to deliver actionable insights.
3,900+ records · 10 SQL queries · 3 tools · 6 business recommendations

Overview:
A complete, reproducible data analytics case study on 3,900+ consumer transaction records. The project follows a structured three-phase pipeline — Python EDA and feature engineering, PostgreSQL business querying, and Power BI interactive dashboard reporting — producing six prioritised, data-backed business recommendations across revenue, product performance, discount effectiveness, customer loyalty, shipping behaviour, and demographic analysis.

Business Context:
Retail businesses accumulate large volumes of transactional data but frequently lack visibility into which customer segments drive revenue, whether loyalty programs are being fully utilised, and where discount strategies are eroding margins. This project addresses those gaps directly — using a 3,900+ record consumer dataset to move from raw transaction data to quantified findings and prioritised commercial recommendations.

Key Findings:
- 2.1× gender revenue gap — Male $157,890 vs Female $75,191 in a category mix where female demand typically leads, pointing to an acquisition funnel gap
- 72% of customers with more than 5 purchases (2,518 people) hold no subscription — the highest-priority conversion audience in the dataset
- Hat (50%), Sneakers (49%), and Coat (49%) carry near-50% discount rates — full-price purchasing is no longer the norm, indicating margin erosion risk
- Young Adults generated the highest revenue at $62,143 across four age groups; all groups fall within a $6,380 range confirming broad demographic appeal
- 839 discount users still spent at or above the $59.76 dataset average — discounts functioning as conversion accelerators, not margin eroders
- 79% of the customer base is Loyal (more than 10 purchases); only 2% are New — strong retention but a critical new-customer acquisition gap

Business Impact:
- 2,518 pre-qualified repeat buyers with no subscription represent an immediately actionable conversion audience — reachable without any new acquisition spend
- Near-50% discount rates on five major SKUs indicate margin is being left on the table; a structured A/B test could recover it without losing conversion volume
- A 2.1× gender revenue gap in a female-dominant product category points to a recoverable acquisition failure, not a product problem
- All six recommendations are directly traceable to specific query outputs, making them measurable and testable — not directional guesses

Tech Stack:
- Python — Pandas, SQLAlchemy
- SQL — PostgreSQL, pgAdmin 4
- Business Intelligence — Microsoft Power BI Desktop

Repository Contents:
- consumer_shopping_behaviour_vscode.ipynb — End-to-end Python EDA pipeline: data ingestion, quality audit, null imputation, feature engineering, and SQLAlchemy ETL load into PostgreSQL
- consumer_shopping_ehaviour_sqlcode.sql — 10 annotated PostgreSQL business queries using aggregations, correlated subqueries, CTEs, conditional aggregation, and ROW_NUMBER() window functions
- customer_shopping_behaviour_dashboard.pbix — Interactive Power BI dashboard, KPI cards, 5 chart visuals, and 4 cross-filter slicers
- Consumer_Shopping_Behaviour_Project_Report.docx/.pdf — Detailed project report covering methodology, all SQL outputs, findings, and recommendations
- Consumer_Shopping_Behaviour_Analytics.pptx/.pdf — Presentation deck 

Methodology:
- Phase 1 — Python EDA: Data ingestion, null audit, category-median imputation on review_rating, column standardisation, redundant feature removal (promo_code_used confirmed 100% identical to discount_applied), feature engineering — age_group via pd.qcut into four equal-frequency quantile bands, purchase_frequency_days via categorical label mapping — and SQLAlchemy ETL load into PostgreSQL.
- Phase 2 — PostgreSQL: 10 business queries in pgAdmin 4 using aggregations, correlated subqueries, CTEs, conditional aggregation (CASE WHEN), and window functions (ROW_NUMBER() OVER (PARTITION BY category)).
- Phase 3 — Power BI: Single-page interactive dashboard with 3 DAX-driven KPI cards, 5 chart visuals, and 4 cross-filter slicers — enabling self-serve stakeholder exploration with no SQL or Python access required.

Business Recommendations:
- HIGH — Launch targeted subscription conversion campaign for the 2,518 repeat non-subscriber cohort with exclusive benefits: free shipping thresholds, early sale access, loyalty points
- HIGH — A/B test reduced discount depths (20%, 30%, current) on Hat, Sneakers, and Coat to find the margin-optimal conversion floor
- MEDIUM — Invest in female-targeted acquisition: gender-focused digital campaigns, influencer partnerships, personalised recommendation engines
- MEDIUM — Strengthen Young Adult retention via mobile-first UX, early sale access, and personalised re-engagement journeys
- LOW — Add a checkout-stage Express shipping upsell nudge tied to a minimum basket threshold (e.g., orders over $75)
- LOW — Feature top-rated products (Gloves 3.86, Sandals 3.84, Boots 3.82) in homepage hero sections and email campaign headers

How to Run:
- Python Notebook
Install dependencies: pip install pandas sqlalchemy psycopg2
Open consumer_shopping_behaviour_vscode.ipynb in Jupyter or VS Code and run all cells in order. Before the database load cell, update the connection string: postgresql+psycopg2://username:password@localhost:5432/your_database_name
- SQL Queries
The customer table must exist in your PostgreSQL database — run the notebook first to create and populate it. Open consumer_shopping_behaviour_sqlcode.sql in pgAdmin 4 and execute queries individually or in full.
- Power BI Dashboard
Requires Microsoft Power BI Desktop (free). Open customer_shopping_behaviour_dashboard.pbix and reconnect the data source to your local PostgreSQL instance or the cleaned CSV if needed.

Skills Demonstrated:
- Data Analysis & Processing
Python · Pandas · SQLAlchemy · Data Cleaning · Exploratory Data Analysis (EDA) · Null Imputation · Feature Engineering · pd.qcut · Label Encoding · ETL Pipeline
- SQL & Data Modelling
PostgreSQL · pgAdmin 4 · CTEs · Window Functions · ROW_NUMBER() · PARTITION BY · CASE WHEN · Conditional Aggregation · Correlated Subqueries · Aggregations
- Business Intelligence
Power BI · KPI Dashboard Design · Data Visualisation · Cross-Filter Slicers · Stakeholder Reporting
- Analytics & Business Thinking
Customer Segmentation · Retail Analytics · Consumer Behaviour Analysis · Discount Strategy · Loyalty Analysis · Revenue Analysis · Demographic Analysis · End-to-End Analytics Pipeline · Reproducible Research
