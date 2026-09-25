# SQL Data Analytics Project

## STAR Format Project Summary

### Situation
This project was built to create a complete SQL-based analytics workflow for a retail data warehouse. The goal was to transform raw sales and dimension data into a structured analytical environment where business questions could be answered through SQL exploration, aggregation, and KPI analysis.

The repository contains a `gold` schema with customer, product, and sales tables. The business challenge was to analyze performance across product categories, customer segments, and revenue drivers using SQL.

### Task
The task was to:
- initialize and structure a SQL database for analytics;
- load curated CSV data into warehouse tables;
- explore the database schema and business dimensions;
- calculate key business metrics and KPIs;
- analyze magnitude and ranking questions across customers and products;
- build a practical analytical foundation using the available SQL workflow.

### Action
The project was implemented as a step-by-step SQL workflow using the scripts currently available in the repository:

1. Database setup and schema creation
   - [scripts/00_init_database.sql](scripts/00_init_database.sql)
   - Creates the `DataWarehouseAnalytics` database and the `gold` schema.
   - Loads the main analytical tables: `dim_customers`, `dim_products`, and `fact_sales`.

2. Data and schema exploration
   - [scripts/01_database_exploration.sql](scripts/01_database_exploration.sql)
   - [scripts/02_dimensions_exploration.sql](scripts/02_dimensions_exploration.sql)
   - [scripts/03_date_range_exploration.sql](scripts/03_date_range_exploration.sql)
   - Helps understand table structure, unique dimension values, and historical date coverage.

3. Core business metrics and analysis
   - [scripts/04_measures_exploration.sql](scripts/04_measures_exploration.sql)
   - [scripts/05_magnitude_analysis.sql](scripts/05_magnitude_analysis.sql)
   - [scripts/06_ranking_analysis.sql](scripts/06_ranking_analysis.sql)
   - Covers sales totals, customer and product counts, revenue distribution, category performance, and top/bottom-ranked entities.

### Result
The final outcome is a focused SQL analytics project that turns rawsales data into a usable business intelligence foundation. It enables:

- sales analysis by total revenue, orders, and items sold;
- customer and product-level performance review;
- measurement of data distribution across dimensions;
- identification of top and weak-performing entities;
- a structured SQL-based workflow for business exploration and KPI reporting.

This project serves as a practical example of how SQL can be used for exploratory analytics and business insight generation.

---

## Project Structure

```text
sql-data-analytics-project/
├── datasets/
│   └── csv-files/
│       ├── gold.dim_customers.csv
│       ├── gold.dim_products.csv
│       ├── gold.fact_sales.csv
│       └── other source files
├── scripts/
│   ├── 00_init_database.sql
│   ├── 01_database_exploration.sql
│   ├── 02_dimensions_exploration.sql
│   ├── 03_date_range_exploration.sql
│   ├── 04_measures_exploration.sql
│   ├── 05_magnitude_analysis.sql
│   └── 06_ranking_analysis.sql
├── README.md
└── LICENSE
```

---

## Data Model

The warehouse is structured around a simple star-like model:

- `gold.dim_customers`: customer demographics and metadata
- `gold.dim_products`: product information, category, and cost details
- `gold.fact_sales`: transactional sales records such as order info, quantity, sales amount, and dates

This structure supports analytical queries that join dimensions to fact tables for reporting and KPI analysis.

---

## How to Run the Project

1. Open SQL Server Management Studio or Azure Data Studio.
2. Run [scripts/00_init_database.sql](scripts/00_init_database.sql) first.
3. Execute the remaining scripts in numerical order from 01 to 06.
4. Review the output of each query to understand the data and business trends.

> Note: the database setup script contains a hardcoded CSV path. If your local environment differs, update the file path in [scripts/00_init_database.sql](scripts/00_init_database.sql) before running it.

---

## Key Analytics Covered

- Database and schema exploration
- Date range and historical coverage checks
- KPI calculations such as revenue, orders, and average price
- Customer and product magnitude analysis
- Ranking of top and low-performing products and customers
- Business distribution analysis by category, country, and customer behavior

---

## Business Value

This project demonstrates how SQL can be used to support business intelligence decisions by:

- measuring overall business performance;
- identifying high-value customers and products;
- highlighting where revenue is concentrated;
- comparing performance across categories and entities;
- providing a foundation for dashboards and management reporting.

---

## License

This project is intended for learning and analytics practice. Please review the relevant licensing details in the repository before commercial reuse.
