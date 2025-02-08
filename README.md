# comprehensive analysis of "Sales Dynamics and Performance Drivers for Adidas


##  Table of Contents
- [Adidas](#Adidas)
- [Business Task](#business-task)
- [Data Source](#data-source)
- [Methodology](#methodology)
- [Data Exploration](#data-exploration)
- [Visualization](#visualization)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)
***

## Adidas

Adidas, founded in 1949, is a global sportswear giant headquartered in Germany. Known for its innovative and high-performance products, the brand offers a wide range of sportswear, footwear, and accessories. The iconic three-stripe logo symbolizes quality and style in various sports, including soccer, running, and basketball. Committed to sustainability and technological advancements, Adidas continuously improves its products and environmental impact. Collaborations with athletes and designers, along with a significant presence in sports culture, make Adidas a leading brand in the industry.

## Business Requirements:

Adidas aims to empower its decision-makers with data-driven insights, fostering strategic growth and competitiveness with :

1.  Enhanced Understanding of Sales Dynamics and Performance Drivers:

    - Conduct comprehensive analysis of key metrics, including total sales, units sold, operating profit, average price per unit, and operating margin.

    - Generate actionable insights into sales trajectories and the factors influencing performance.

2. Identification of Geographical Areas with High and Low Sales Potential:

    - Evaluate sales performance across various regions, states, and cities to pinpoint areas of strong and weak sales.

    - Utilize these insights to guide targeted marketing and inventory decisions.

3. Insights into Product Performance:

    - Assess the performance of different product categories (e.g., footwear, apparel) to determine their impact on overall sales and profitability.

    - Identify high-demand and underperforming products to aid in effective inventory and marketing strategies.

4. Insights into Retailers Performance

   -

5. Actionable Recommendations for Optimizing Sales and Profits Across Various Dimensions:

    - Develop strategic recommendations based on thorough analysis to enhance sales and profitability.

## Data Source

Adidas Sales Data: The primary data used for this analysis "Adidas Sales Data.csv" file, contains detailed information about each sale made by the company
[data link](https://github.com/grandady/Bank-loan/blob/main/financial_loan.csv)

Methodology

This project employs a rigorous, tool-specific methodology leveraging SQL for end-to-end data management and Power BI for advanced analytics and visualization. The process is structured into four phases to ensure systematic execution and alignment with business objectives:

1. Data Collection & Extraction (SQL-Centric)

1.1 Data Source Identification

Adidas Internal Sales Data: Transactional records, regional sales performance, product SKU details, pricing structures, and channel-specific metrics from Adidas’s enterprise databases.

1.2 SQL-Driven Data Extraction

Targeted Query Design: Developed granular SQL queries to extract structured datasets, filtering by time periods (e.g., fiscal quarters), geographies (regions/states/cities), product categories, and sales channels.

Key Metrics Extraction: Explicitly included fields such as total_sales, units_sold, operating_profit, price_per_unit, and operating_margin to support profitability and efficiency analyses.

Cross-Dimensional Data Pull: Utilized SQL JOIN operations to integrate relational tables (e.g., linking product IDs to regional sales) and GROUP BY clauses to aggregate data at required granularities (monthly, category-level).

2. Data Preparation & Transformation

2.1 Data Cleaning (SQL)

Null Handling: Applied SQL COALESCE functions and CASE statements to address missing values, ensuring completeness in critical fields like region and product_category.

Consistency Checks: Standardized data formats (e.g., converting strings to DATE types for time-based analysis) and validated numeric ranges (e.g., non-negative units_sold).

Duplicate Removal: Executed SQL DISTINCT and ROW_NUMBER() window functions to eliminate redundant records.

2.2 Data Transformation

SQL-Based Aggregation: Pre-aggregated metrics (e.g., monthly sales by region) using SUM() and AVG() functions to optimize downstream processing in Power BI.

Power Query (Power BI):

Merged supplementary datasets (e.g., regional demographics) using GUI-driven joins.

Created calculated columns (e.g., profit_per_unit = operating_profit / units_sold) for granular insights.

Implemented star schema design with fact/dimension tables to enhance model performance.

3. Data Analysis & Modeling (Power BI)
3.1 Data Model Optimization

Established relationships between fact tables (sales transactions) and dimension tables (products, regions, dates) for seamless cross-filtering.

Configured role-playing dimensions (e.g., Order Date vs. Ship Date) for time intelligence analysis.

3.3 Analytical Techniques

Trend Analysis: Identified seasonality and growth patterns using line charts with moving averages.

Regional Performance: Compared operating margins across states via clustered bar charts and map visuals.

Product Portfolio Analysis: Evaluated sales concentration with ABC classification (Pareto principle).


4. Visualization & Reporting (Power BI)
4.1 Interactive Dashboard Development

Built executive-facing dashboards with drill-through capabilities (e.g., regional → city-level sales).

Designed tooltips for contextual metadata (e.g., product descriptions on hover).

Incorporated slicers for dynamic filtering by date, region, and product category.

4.2 Actionable Insights Delivery

Highlighted underperforming regions and overstocked product categories using conditional formatting.

Created a “Profitability Scorecard” with KPI cards for real-time monitoring of margins and sales targets.

4.3 Deployment & Collaboration

Published reports to Power BI Service for secure, role-based access across stakeholders.

Enabled automated data refresh schedules to maintain report accuracy.

Documented SQL queries and DAX logic in a centralized repository for transparency and scalability.

