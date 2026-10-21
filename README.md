# E-commerce Retail Analytics Using PySpark and Databricks

## Project Overview

An end-to-end data engineering and analytics project built using PySpark and Databricks to process, clean, validate, and analyze online retail transaction data.

The project demonstrates distributed data processing, reusable ETL pipeline functions, Delta Lake storage, Spark SQL analytics, automated data-quality validation, scheduled pipeline execution, and an interactive sales dashboard.

## Dataset

- **Dataset:** UCI Online Retail
- **Original records:** 541,909
- **Original columns:** 8
- **Exact duplicate records removed:** 5,268
- **Cleaned records:** 536,641
- **Data period:** December 2010 – December 2011 (through December 9, 2011)

The dataset contains online retail transactions, including invoice numbers, product descriptions, quantities, invoice dates, unit prices, customer IDs, and countries.

The dataset is not included in this repository. Obtain it from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail).

## Technologies Used

- Python
- Apache Spark / PySpark
- Databricks Notebooks
- Spark SQL
- Delta Lake
- Databricks SQL and AI/BI Dashboards
- Databricks Jobs
- Git and GitHub
- Matplotlib

## Project Architecture

1. Load the original CSV dataset into Spark.
2. Inspect the data and identify duplicates, missing values, and invalid records.
3. Remove exact duplicate records.
4. Normalize text columns and create data-quality flags.
5. Calculate transaction revenue using quantity × unit price.
6. Validate required fields, duplicate counts, and revenue calculations.
7. Save the cleaned dataset as a Delta table.
8. Build reusable loading, cleaning, validation, and saving functions.
9. Execute the workflow through a single `run_pipeline()` function.
10. Analyze revenue by country, product, and month using Spark SQL.
11. Create a monthly sales summary.
12. Build and publish an interactive sales analytics dashboard.
13. Configure a Databricks Job for pipeline execution.

## Data Quality Results

| Validation | Result |
|---|---:|
| Original records | 541,909 |
| Cleaned records | 536,641 |
| Exact duplicates removed | 5,268 |
| Remaining exact duplicates | 0 |
| Missing invoice numbers | 0 |
| Missing invoice dates | 0 |
| Incorrect revenue calculations detected | 0 |

All five implemented data-quality tests passed successfully.

## Key Results

- Processed 541,909 original transaction records.
- Retained 536,641 records after removing exact duplicates.
- Stored cleaned data in the `cleaned_online_retail` Delta table.
- Created a reusable PySpark ETL pipeline.
- Created the `monthly_sales_summary` table.
- Calculated total recorded revenue of **9,726,006.95 dataset currency units**.
- Identified November 2011 as the highest-revenue month, with 1,456,145.80 recorded revenue units.
- Identified the United Kingdom as the leading revenue-generating country in the analysis.
- Built and published the **E-commerce Sales Analytics Dashboard**.

## Dashboard

The dashboard includes:

- **Total Revenue:** Overall recorded revenue.
- **Total Orders:** Distinct invoice count.
- **Monthly Revenue Trend:** Revenue changes over time.
- **Revenue by Country:** Comparison of revenue across countries.
- **Top 10 Products by Revenue:** Ranking by recorded revenue.

The product ranking can include postage-related items, so postage charges should be considered when interpreting merchandise performance.

## Business Insights

- Country-level analysis highlights the primary revenue-generating markets.
- Product-level analysis identifies items with high recorded revenue.
- Monthly analysis reveals changes in sales over time.
- Revenue increased substantially from September through November 2011.
- November 2011 recorded the highest monthly revenue in the dataset.
- December 2011 contains data only through December 9, making it an incomplete month that should not be directly compared with full months.
- Excluding postage charges from merchandise comparisons can provide a clearer view of product performance.

## How to Run

1. Open `Ecommerce_Retail_Analytics.ipynb` in Databricks.
2. Download the UCI Online Retail dataset and upload the CSV file to your Databricks workspace.
3. Update the `file_path` variable to point to your uploaded CSV.
4. Run the notebook cells in order.
5. Execute `run_pipeline(file_path)`.
6. Review the data-quality validation output.
7. Inspect the cleaned Delta table and monthly sales summary.
8. Explore the dashboard after configuring the appropriate Databricks compute resources.

**Note:** The notebook currently uses a workspace-specific file path. Users must upload the dataset and configure their own path before running the pipeline.

## Future Improvements

- Add structured logging and more robust exception handling.
- Expand automated unit tests for individual transformation functions.
- Add dashboard filters for country, product, and date range.
- Improve configuration management to make the pipeline easier to reuse across workspaces.
- Add screenshots and a visual architecture diagram to the repository.

## Repository Contents

- `Ecommerce_Retail_Analytics.ipynb` — data cleaning, validation, transformation, and analytics.
- `README.md` — project overview, workflow, results, and setup instructions.
- `.gitignore` — files excluded from version control.

The retail dataset is not included in the repository; download it from the UCI Machine Learning Repository.

## Author

**Surbhi Aglawe**
