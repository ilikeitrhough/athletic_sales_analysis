# Athletic Sales Analysis

## Overview
This project analyzes sales data to gain insights into which cities in the U.S. have sold the most athletic wear over two years. It also determines which retailers had the greatest total sales for athletic wear, which retailers sold the most women's athletic footwear, and identifies the days and weeks with the highest sales for women's athletic footwear.

## Getting Started

### Prerequisites
- Python 3.7+
- Pandas library

### Installation
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/ilikeitrhough/athletic_sales_analysis.git

2. Navigate to the project directory:

   ```bash
    cd athletic_sales_analysis
    Install the necessary dependencies:
   ```
3. Install the necessary dependencies:
   ```bash
    pip install pandas
   ```
### Files
athletic_sales_2020.csv: Sales data for the year 2020.\
athletic_sales_2021.csv: Sales data for the year 2021.\
analysis.py: Script to perform the analysis.

### Usage
Ensure that the CSV files (athletic_sales_2020.csv and athletic_sales_2021.csv) are in the project directory.\
Run the analysis.py script:
   ```bash
python analysis.py
   ```
### Analysis Steps
1. Combine and Clean the Data
* Import the two CSV files and read them into DataFrames.
* Combine the DataFrames by the rows and reset the index.
* Check for null values and convert the invoice_date column to a datetime data type.
2. Determine which Region Sold the Most Products
* Use pivot_table to create a multi-index DataFrame with region, state, and city columns.
* Aggregate the data to find the total number of products sold.
* Sort the results in descending order to show the top five regions.
3. Determine which Region had the Most Sales
* Use pivot_table to create a multi-index DataFrame with region, state, and city columns.
* Aggregate the data to find the total sales.
* Sort the results in descending order to show the top five regions.
4. Determine which Retailer had the Most Sales
* Use pivot_table to create a multi-index DataFrame with retailer, region, state, and city columns.
* Aggregate the data to find the total sales.
* Sort the results in descending order to show the top five retailers.
5. Determine which Retailer Sold the Most Women's Athletic Footwear
* Filter the DataFrame to include only women's athletic footwear sales data.
* Use pivot_table to create a multi-index DataFrame with retailer, region, state, and city columns.
* Aggregate the data to find the total number of women's athletic footwear units sold.
Sort the results in descending order to show the top five retailers.
6. Determine the Day with the Most Women's Athletic Footwear Sales
* Create a pivot table with invoice_date as the index and total_sales as the values.
* Resample the data into daily bins and calculate the total sales for each day.
* Sort the results in descending order to show the top ten days.
7. Determine the Week with the Most Women's Athletic Footwear Sales
* Resample the daily sales data into weekly bins and calculate the total sales for each week.
* Sort the results in descending order to show the top ten weeks.

### Results
The results of the analysis are printed to the console. You can modify the script to save the results to a file or further visualize the data using plots.

### License
This project is licensed under the MIT License.

### Acknowledgments
Thanks to the contributors of the Pandas library for providing the tools necessary for data analysis.
