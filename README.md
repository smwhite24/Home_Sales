# Home Sales Data Analysis with SparkSQL

## Project Overview

This project uses SparkSQL to analyze and determine key metrics about home sales data. Through this challenge, I will create temporary views, partition data for efficient processing, and manage caching to optimize performance. This project demonstrates practical applications of SparkSQL and caching techniques to handle large datasets effectively.

## Goals

The primary objectives of this project include:

1. **Analyzing Key Metrics**: Use SparkSQL to compute essential metrics from the home sales data, such as average sale price, median sale price, and sales trends over time.

2. **Creating Temporary Views**: Utilize Spark to create temporary views of the data, allowing for more flexible and modular data manipulation.

3. **Data Partitioning**: Partition the dataset to improve query performance, especially when handling large volumes of data.

4. **Caching and Uncaching Tables**: Cache temporary tables to speed up repetitive operations, then uncache them to release memory and optimize resource usage.

5. **Verification of Uncached Table**: Confirm that the cached table has been successfully uncached to ensure memory is being managed effectively.

Setup
Prerequisites
Google Colab: This project was executed on Google Colab for ease of use with Spark.
Apache Spark: Version 3.0 or higher, installed in the Colab environment.
Python: For implementing and running SparkSQL queries in Colab.


### Dataset
The project uses a dataset containing information about home sales, including fields such as sale price, date of sale, location, and property characteristics.

### Clone the Repository:

git clone <repo_url>
cd home-sales-data-analysis


Run the Spark Application: Follow the instructions in home_sales_colab.ipynb to execute the Spark job in Google Colab.

## Steps

### Step 1: Load and Explore the Data
- Use Spark to load the dataset and explore its structure.
- Identify key columns relevant to the analysis, such as `Price`, `sqft_living`, ``, and `Bedrooms`.

### Step 2: Data Transformation and Analysis with SparkSQL
- Create temporary views using SparkSQL to simplify querying.
- Write SQL queries to determine key metrics like:
  - **Average Sale Price**: Calculate the average sale price of homes.
  - **Median Sale Price**: Use SparkSQL functions to get the median sale price.
  - **Sales Trends**: Analyze how home sales vary by month, year, or region.

### Step 3: Data Partitioning
- Partition the data based on one or more fields, such as `DateBuilt`, to improve query efficiency and parallel processing.

### Step 4: Caching and Uncaching
- **Cache** the temporary table to speed up repeated queries and calculations.
- Execute SparkSQL operations using the cached data.
- **Uncache** the table to free up memory after analysis is complete.

### Step 5: Verification
- Verify that the table has been successfully uncached by attempting to reference it post-uncache.

## Usage Example

To run a sample query, use the following command:

```python
# Sample SparkSQL query to calculate average sale price
spark.sql("SELECT AVG(SalePrice) AS avg_sale_price FROM home_sales").show()
```

## Results

The final output will include key metrics on home sales, performance improvements from data partitioning, and effective use of caching and uncaching for memory management.

## Resources
-  Boot Camp class activities and notes
-  Xpert Learning Assistant to hekp troubleshoot code and query formats.
