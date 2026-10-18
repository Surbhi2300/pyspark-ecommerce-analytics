
# E-commerce Retail Analytics Using PySpark and Databricks

## Project Overview
An end-to-end data analytics project using PySpark and Databricks to clean, validate, and analyze online retail transaction data. The project demonstrates distributed data processing, Delta table storage, Spark SQL, and business-oriented sales analysis.

## Dataset
- **Dataset:** UCI Online Retail
- **Original records:** 541,909
- **Original columns:** 8
- **Records after exact duplicate removal:** 536,641

## Technologies
- Python
- Apache Spark / PySpark
- Databricks
- Spark SQL
- Delta Lake
- CSV

## Project Workflow
1. Load the retail CSV dataset into Spark.
2. Profile missing values and duplicate records.
3. Remove exact duplicate rows.
4. Normalize text columns and create data-quality flags.
5. Calculate revenue using quantity multiplied by unit price.
6. Save the cleaned dataset as a Delta table.
7. Analyze revenue by country, product, and month.
8. Use Spark SQL for business queries.
9. Validate duplicate counts, required fields, revenue calculations, and row counts.
10. Save a reusable monthly sales summary table.

## Key Results
- Processed 541,909 original records.
- Removed 5,268 exact duplicate rows.
- Retained 536,641 records in the cleaned dataset.
- Identified the United Kingdom as the highest-revenue country.
- Identified November 2011 as the highest-revenue month in the dataset.
- Passed the implemented data-quality validation checks.

## Business Insights
- Country-level analysis identifies the main revenue-generating markets.
- Product-level analysis identifies high-revenue merchandise.
- Monthly analysis highlights changes in recorded revenue over time.
- Postage charges can be separated from merchandise for clearer product comparisons.

## Future Improvements
- Add automated pipeline execution and scheduling.
- Implement structured logging and exception handling.
- Add automated tests for data quality.
- Build a sales dashboard.
- Document reproducible setup and execution instructions.
