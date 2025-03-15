# Power BI Sales Report - Well Rock Company

## Project Overview
This project focuses on creating a comprehensive Sales Report Dashboard for Well Rock Company using Power BI. The report is designed to provide key sales insights with interactive visualizations, supporting data-driven decision-making.

## Business Requirement Document (BRD)
The project follows the Business and Functional Requirement Document (BRD), ensuring that all necessary data is integrated, modeled, and visualized correctly.

## Data Sources
The data used in this project comes from multiple sources:
- **Sales Data** (Folder containing yearly sales files)
- **Categories** (Excel)
- **Geography** (Excel)
- **Product** (SQL Database)
- **SalesRep** (Excel)
- **SubCategories** (Excel)

---
## Project Tasks

### 1. Data Gathering & Preparation
- Load all sales files into a single Sales Fact Table with a resilient mechanism:
  - Removing a file should not cause errors.
  - Adding a new yearly file should be automatically included on refresh.

### 2. Data Modeling
- Transform Sales Fact Table:
  - Split Country and City from "Location" field and assign correct data type for Geo maps.
  - Ensure the correct date format is applied.
- Create a unique key (**GeoKey**) in Sales and Geography tables.
- Clean ID columns in **SalesRep** and **SubCategories** tables by removing the prefix "ID - " using a reusable function.
- Establish relationships between all tables using a Calendar table for date-based analysis.

### 3. DAX Calculations
- **Total Revenue** = Product’s Retail Price * Units Sold.
- **Total Cost** = Product’s Standard Cost * Units Sold.
- **Gross Profit** = Total Revenue - Total Cost.
- **Gross Profit MoM Growth (%)** to analyze month-over-month changes.
- **Average Sales per Day** = Total Revenue / Number of Sales Days.
- **Product Breakdown Analysis** to identify drops or increases in product sales.
- **Quarter-over-Quarter (QoQ) Growth Analysis** to support the QBR (Quarterly Business Review) report.

### 4. Report & Visualization
- Develop a one-page **Power BI Sales Dashboard** showcasing:
  - Sales performance trends.
  - Geo-based sales insights.
  - Product and category performance analysis.
  - Monthly and quarterly growth trends.
- Ensure that months on the X-axis are sorted from **January to December**.

## Final Deliverables
- Power BI Dashboard (.pbix file)
- Data Model with relationships
- DAX Calculations for KPI tracking
- Functional Report Layout

## Tools & Technologies Used
- **Power BI** for data visualization and reporting
- **Power Query** for data transformation
- **DAX (Data Analysis Expressions)** for calculated measures
- **Excel & CSV files** for data sources

## Future Enhancements
- Automate data refresh for seamless updates.
- Enhance the dashboard with additional insights like regional performance comparisons.
- Implement predictive analysis for future sales trends.

