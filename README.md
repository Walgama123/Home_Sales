<h1 align="center"> Home Sales Analysis with SparkSQL </h1>

<div align="center">
	<img src="images/icon.png">
</div>


## Overview
This project involves analyzing home sales data using SparkSQL to determine key metrics such as average prices based on various criteria. The project includes creating temporary views, partitioning data, caching tables, and optimizing query performance using PySpark.

## Repository Structure
- Home_Sales.ipynb: Jupyter notebook containing the code for data analysis and answering the challenge questions.
- [home_sales_revised.csv: The dataset containing home sales information used for the analysis.](https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv)
- README.md: This file, providing an overview and instructions for the project.

## Prerequisites
- [Apache Spark](https://spark.apache.org/)
- [PySpark](https://spark.apache.org/docs/latest/api/python/index.html)
- [Jupyter Notebook](https://docs.jupyter.org/en/latest/)
- [Python 3.x](https://www.python.org/downloads/)

# Project Setup
- Clone the Repository: git clone https://github.com/Walgama123/Home_Sales.git

- Navigate to the Project Directory: cd Home_Sales

- Install the Required Python Packages: 
  - pip install <required packages >
- Launch Jupyter Notebook: jupyter notebook


## Instructions
1. Read the Data:
  - Load the home_sales_revised.csv dataset into a Spark DataFrame. 
2.Create Temporary Table:
  - Create a temporary table called home_sales from the DataFrame.
3.Query the Data:

  - Execute queries to determine:
    - The average price for a four-bedroom house sold each year.
    - The average price of a home with three bedrooms and three bathrooms for each year the home was built.
    - The average price of a home with three bedrooms, three bathrooms, two floors, and at least 2,000 square feet for each year the home was built.
    - The average price of a home per "view" rating with an average home price of at least $350,000.
4. Cache and Uncache the Table:
- Cache the home_sales table and verify it is cached.
- Run the last query on the cached table and compare the runtime with the uncached table.

5. Partition and Parquet Format:
- Partition the dataset by the date_built field and save it in Parquet format.
- Create a temporary table from the Parquet data and run the last query again, comparing the runtime.

6.Uncache the Table:
- Uncache the home_sales table and verify it is uncached.