# Home Sales Analysis with SparkSQL

![stockmarket](https://github.com/SakinaJaffri/Home_Sales/assets/146900226/c1c3242e-d11f-424d-8d64-248545246201)


## Overview
This project involves analyzing home sales data using SparkSQL to derive key insights and metrics. The tasks include creating temporary views, partitioning data, caching tables for optimized queries, and evaluating query performance.

## Workflow Summary
1. Imported necessary PySpark SQL functions.
2. Read the 'home_sales_revised.csv' data into a Spark DataFrame.
3. Created a temporary table named 'home_sales' for data analysis.

### Key Questions Answered:
- **Average Price for Four-Bedroom Houses by Year**
  - Calculated the average price for four-bedroom houses sold each year, rounded to two decimal places.

- **Average Price of Homes Built by Specific Criteria**
  - Determined the average price for homes built in specific conditions (e.g., 3 bedrooms, 3 bathrooms) per year, rounded to two decimal places.

- **Average Price of Homes with Detailed Criteria**
  - Evaluated the average price for homes meeting detailed criteria (3 bedrooms, 3 bathrooms, two floors, ≥ 2,000 sqft) per year, rounded to two decimal places.

- **Average Price of Homes by View Rating**
  - Analyzed the average price of homes per "view" rating with an average home price of ≥ $350,000, capturing query runtime in seconds, rounded to two decimal places.

4. Cached the 'home_sales' temporary table for query optimization.

5. Validated table caching and executed the query related to average home price by view rating using the cached data, achieving a reduced runtime compared to uncached operations.

6. Partitioned the formatted home sales data by the 'date_built' field into Parquet format.

7. Created a temporary table for the Parquet data and executed a query for average home price by view rating using partitioned data, noting the impact on query runtime due to partitioning strategy.

8. Uncached the 'home_sales' temporary table to release cached memory resources.

9. Verified the uncaching of the 'home_sales' temporary table using PySpark functionality.

This project demonstrates the use of SparkSQL capabilities for data analysis, including data manipulation, optimization strategies, and performance evaluation with real-world home sales data. Adjusting data partitioning and caching strategies can significantly impact query runtime and resource utilization.
