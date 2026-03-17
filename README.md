# Sales-Operations-Dashboard
End-to-end sales analysis using SQL and Power BI

Sales Performance Analysis Project

This project demonstrates a comprehensive sales data analysis workflow, from raw data generation and cleaning to insightful reporting and data visualisation. It utilises Python with `pandas` for data manipulation, `sqlite3` for database integration, and `matplotlib` for basic visualisations. The final output includes a master dataset suitable for Business Intelligence (BI) tools.

 Table of Contents

- Project Overview(project-overview)
- Setup and Prerequisites(setup-and-prerequisites)
- Project Steps & Analysis(project-steps--analysis)

  - 1. Data Generation & Initial Cleanup(1-data-generation--initial-cleanup)
  - 2. Database Integration(2-database-integration)
  - 3. Performance Analysis - Sales vs. Targets(3-performance-analysis---sales-vs-targets)
  - 4. Category Performance(4-category-performance)
  - 5. Monthly Sales Growth Analysis(5-monthly-sales-growth-analysis)
  - 6. Identifying Regions Below Target(6-identifying-regions-below-target)
  - 7. High-Value Transactions(7-high-value-transactions)
  - 8. Visualizing Regional Performance(8-visualizing-regional-performance)
  - 9. Final Data Export(9-final-data-export)

- Usage(usage)
- Generated Files(generated-files)

Project Overview

This project aims to provide a structured approach to sales data analysis. We simulate a typical 'messy' sales dataset, demonstrate robust data cleaning techniques, integrate with a SQL database, perform various analytical queries to uncover business insights, and prepare a unified dataset for advanced BI tools.

Setup and Prerequisites

To run this notebook, you will need the following Python libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `sqlite3` (usually built-in with Python)

You can install these using pip:
```bash
pip install pandas numpy matplotlib
```

Project Steps & Analysis

 1. Data Generation & Initial Cleanup
The project begins by generating synthetic sales data, intentionally introducing missing values and duplicates to simulate real-world data challenges. This raw data is then cleaned to ensure accuracy and consistency.

Key Cleaning Steps:

*   Duplicate Removal: Ensures each transaction is unique.
*   Missing Value Imputation: Fills missing sales amounts with the average and missing regions with 'Unknown'.
*   Date Standardisation: Converts date columns to datetime objects and extracts month names.

 2. Database Integration
The cleaned sales data (`df_sales`) and the sales targets (`targets`) are loaded into an SQLite database for efficient querying and relational analysis.

 3. Performance Analysis - Sales vs. Targets
This analysis compares actual sales against target amounts by region and month, calculating variance and variance percentage.

 4. Category Performance
An overview of sales performance by product category, including total revenue, total orders, and average order value.

 5. Monthly Sales Growth Analysis
Calculates month-over-month sales growth to identify trends and momentum.

 6. Identifying Regions Below Target
Highlights specific regions and months where sales fell short of their targets, indicating areas that require attention.

 7. High-Value Transactions
Identifies and segments high-value transactions based on their amount, helping to understand significant sales events.

 8. Visualising Regional Performance
Generates a bar chart to visually compare actual sales against target amounts for each region.

 9. Final Data Export
A master CSV file is generated, combining sales and target data into a single, unified dataset, ideal for Business Intelligence tools like Power BI.

 Usage

To run this project:
1.  Open the `.ipynb` notebook in Google Colab or Jupyter Notebook.
2.  Run all cells sequentially.
3.  The notebook will generate `sales_data.csv`, `targets.csv`, and `final_project_data.csv` locally, and create an SQLite database `sales_company.db`.
4.  The final `final_project_data.csv` will be automatically downloaded in Colab.

 Generated Files
-   `sales_data.csv`: The initial messy sales data.
-   `targets.csv`: The clean target data.
-   `sales_company.db`: An SQLite database containing `sales_table` and `target_table`.
-   `final_project_data.csv`: The cleaned and merged dataset, ready for BI tools.
