# Home Sales Analysis with SparkSQL

![Home Sales](https://github.com/SakinaJaffri/Home_Sales/assets/146900226/c1c3242e-d11f-424d-8d64-248545246201)

## Overview

This project focuses on analyzing home sales data using **SparkSQL**. It involves creating temporary views, partitioning data, caching tables for optimization, and evaluating query performance using PySpark SQL. The goal is to derive insights into home sales trends based on various metrics and criteria.

## Workflow Summary

1. **Data Loading**: 
   - Imported necessary PySpark SQL functions.
   - Loaded the `home_sales_revised.csv` dataset into a Spark DataFrame.
   - Created a temporary view called `home_sales` for SQL-based data analysis.

2. **Data Analysis**:
   - **Average Price for Four-Bedroom Houses by Year**: Calculated the average price of four-bedroom homes sold each year.
   - **Average Price by Specific Criteria**: Analyzed average home prices based on conditions like the number of bedrooms, bathrooms, square footage, and other factors.
   - **Price by View Rating**: Assessed the average price of homes based on their "view" rating for homes with prices above $350,000, while capturing query runtimes.

3. **Performance Optimization**:
   - **Caching**: Cached the `home_sales` temporary table to optimize queries for better performance.
   - **Partitioning**: Partitioned the dataset by the `date_built` field and saved it in Parquet format to optimize performance on large datasets.
   - **Uncaching**: Released cached memory after analysis.

4. **Query Runtime Evaluation**:
   - Measured the query performance before and after caching the data and analyzed the impact of partitioning on the runtime for querying large datasets.

## Key Insights

- Calculated and analyzed average home prices by year, number of bedrooms, bathrooms, square footage, and view rating.
- Demonstrated the importance of caching and partitioning in reducing query runtime and optimizing resource usage when working with large datasets.

## Technologies Used

- **PySpark**
- **SparkSQL**
- **Pandas**
- **Parquet Format**

## How to Run

1. Clone the repository to your local machine.
2. Install PySpark and other required dependencies listed in `requirements.txt`.
3. Load the dataset and execute the provided PySpark SQL queries in a Jupyter Notebook or PySpark environment.
4. Analyze the home sales data and experiment with different optimization techniques.

## Conclusion

This project showcases the power of SparkSQL in handling large datasets efficiently through query optimization techniques such as caching and partitioning. It demonstrates the significant impact of these techniques on reducing query runtimes and improving overall data analysis performance.

## Contributors

- **Sakina Jaffri** - Project Developer
