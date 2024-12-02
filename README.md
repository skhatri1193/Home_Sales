
### Home Sales Analysis with PySpark

This repository contains a project for analyzing home sales data using PySpark. The goal is to leverage SparkSQL to compute key metrics, optimize queries with caching, and partition the dataset to enhance performance. By completing this project, you'll demonstrate proficiency in PySpark and its SQL capabilities, including temporary views, caching, and file partitioning.

---

## Project Overview

The **Home Sales** project involves working with a dataset of home sales to answer key business questions and explore PySpark's performance features. You will work through the following steps:

1. Load and preprocess the dataset using PySpark.
2. Perform data analysis using SQL queries.
3. Cache and uncache tables for performance comparison.
4. Partition the dataset for optimized querying.
5. Compare query runtimes on cached and partitioned data.

---

## Files Included

* **`Home_Sales.ipynb`** : The main Jupyter Notebook containing all the steps, code, and results for this project.
* **`home_sales_revised.csv`** : The dataset used in this project.
* **README.md** : This file, documenting the project structure and implementation details.

---

## Requirements

Before running this project, ensure you have the following:

* Python 3.x
* Apache Spark 3.x
* Jupyter Notebook
* PySpark installed in your environment
* Dataset: `home_sales_revised.csv` (included in the repository)

---

## Key Tasks and Queries

### Data Preparation

1. **Import Data** : Load the `home_sales_revised.csv` file into a Spark DataFrame.
2. **Create Temporary Table** : Create a temporary table named `home_sales`.

### Analysis with PySparkSQL

Answer the following questions:

1. **Average Price for Four-Bedroom Houses**
   Calculate the average price for four-bedroom houses sold for each year, rounded to two decimal places.
2. **Three-Bedroom, Three-Bathroom Houses**
   Calculate the average price of homes built each year with three bedrooms and three bathrooms, rounded to two decimal places.
3. **Three-Bedroom, Three-Bathroom, Two-Floor Houses**
   Calculate the average price of homes built each year with three bedrooms, three bathrooms, two floors, and a minimum of 2,000 square feet, rounded to two decimal places.
4. **Average Price by View Rating**
   Calculate the average price of homes per "view" rating where the average home price is greater than or equal to $350,000. Record the query runtime.

### Caching and Optimization

5. **Cache Table** : Cache the `home_sales` table and validate.
6. **Query Performance** : Rerun the "view rating" query on the cached table and compare the runtime to the uncached query.

### Partitioning and Parquet Format

7. **Partition Data** : Partition the dataset by the `date_built` field and save it in Parquet format.
8. **Create Parquet Table** : Create a temporary table from the Parquet file.
9. **Query Performance on Partitioned Data** : Rerun the "view rating" query and compare the runtime with previous runs.

### Final Steps

10. **Uncache Table** : Uncache the `home_sales` table and verify.

---

## Results and Observations

1. **Optimized Query Execution** : Caching and partitioning significantly improved query runtime.
2. **Data Insights** : Key metrics about home sales by year, features, and view ratings were calculated and analyzed.
