# E-commerce Retail Analytics Using PySpark and Databricks

## Project Overview
An end-to-end data analytics project built using PySpark and Databricks to clean, validate, transform, and analyze online retail transaction data. The project demonstrates distributed data processing, reusable data pipeline functions, Delta Lake storage, Spark SQL, data-quality validation, and business-oriented sales analysis.

## Dataset
- **Dataset:** UCI Online Retail
- **Original records:** 541,909
- **Original columns:** 8
- **Exact duplicate records removed:** 5,268
- **Records after duplicate removal:** 536,641
- **Data period:** December 2010 – December 2011 (through December 9, 2011)

The dataset contains online retail transactions, including invoice numbers, product descriptions, quantities, transaction dates, unit prices, customer IDs, and countries.

## Technologies
- Python
- Apache Spark / PySpark
- Databricks Notebooks
- Spark SQL
- Delta Lake
- CSV
- Matplotlib

## Project Workflow
1. Load the retail CSV dataset into Spark.
2. Profile missing values, duplicate records, and data-quality issues.
3. Remove exact duplicate rows.
4. Normalize text columns and create data-quality flags.
5. Calculate transaction revenue using quantity multiplied by unit price.
6. Validate required fields, duplicate counts, and revenue calculations.
7. Save the cleaned dataset as a Delta table.
8. Build reusable functions for loading, cleaning, validation, and saving.
9. Run the complete workflow using a single `run_pipeline()` function.
10. Analyze revenue by country, product, and month.
11. Use Spark SQL for business queries.
12. Create a monthly sales summary and visualize revenue trends.

## Data Quality Results
- **Original records:** 541,909
- **Cleaned records:** 536,641
- **Exact duplicates removed:** 5,268
- **Remaining exact duplicates:** 0
- **Missing invoice numbers:** 0
- **Missing invoice dates:** 0
- **Incorrect revenue calculations detected:** 0

The implemented validation checks passed successfully.

## Key Results
- Processed 541,909 original transaction records.
- Retained 536,641 records after exact duplicate removal.
- Saved cleaned data in the `cleaned_online_retail` Delta table.
- Created a reusable PySpark pipeline to load, clean, validate, and save data.
- Created a monthly sales summary table named `monthly_sales_summary`.
- Identified November 2011 as the highest-revenue month, with recorded revenue of **1,456,145.80**.
- Calculated total recorded revenue of **9,726,006.95** across the cleaned dataset.
- Identified the United Kingdom as the highest-revenue country in the analysis.

## Business Insights
- Country-level analysis highlights the main revenue-generating markets.
- Product-level analysis identifies high-revenue merchandise.
- Monthly analysis reveals changes in recorded revenue over time.
- Revenue increased substantially from September through November 2011.
- December 2011 contains data only through December 9, so it is an incomplete month and should not be directly compared with full months.
- Postage charges can be excluded from merchandise comparisons for a clearer view of product performance.

## How to Run
1. Open the `Ecommerce_Retail_Analytics.ipynb` notebook in Databricks.
2. Upload the UCI Online Retail CSV file to your Databricks workspace.
3. Update the `file_path` variable to match the location of your uploaded CSV file.
4. Run the notebook cells in order to define the loading, cleaning, and validation functions.
5. Execute `run_pipeline(file_path)` to run the complete workflow.
6. Review the validation output, Delta table, monthly summary, and revenue visualization.

**Note:** The project currently uses a Databricks workspace file path. A new user must upload the dataset and configure the path for their own workspace.

## Future Improvements
- Schedule automatic pipeline execution using Databricks Jobs or Apache Airflow.
- Add structured logging and more robust exception handling.
- Implement automated unit tests for data transformations and validation.
- Build an interactive sales dashboard.
- Improve reproducibility with detailed setup instructions and pipeline configuration.

## Project Repository
The repository contains the Databricks notebook and project documentation. The retail dataset is not included in the repository; obtain it from the UCI Machine Learning Repository.

## Author
Surbhi Aglawe
