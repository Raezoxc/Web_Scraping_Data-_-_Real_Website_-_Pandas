# Web Scraping for List of Largest Companies in the United States by Revenue

## Overview

This Python script scrapes data from Wikipedia's page on the list of largest companies in the United States by revenue. It utilizes BeautifulSoup and requests libraries to fetch and parse HTML content, then processes the data into a Pandas DataFrame and saves it as a CSV file.

## Requirements

- Python 3.x
- BeautifulSoup
- requests
- pandas

## Usage

1. Ensure you have Python installed on your system.
2. Install the required libraries by running:
3. Run the Python script `scrape_companies.py`.

## Code Description
**Importing Libraries:** The script imports necessary libraries such as BeautifulSoup for web scraping, requests for making HTTP requests, and pandas for data manipulation.

**Fetching HTML Content:** It sends an HTTP GET request to the Wikipedia page containing the list of largest companies in the United States by revenue and retrieves the HTML content.

**Parsing HTML Content:** BeautifulSoup is used to parse the HTML content and create a BeautifulSoup object called 'soup'.

<img width="502" alt="image" src="https://github.com/Raezoxc/Web_Scraping_Data_-Python_Pandas/assets/153198226/1437fe74-8b9b-4b29-9425-1036ddadb28f">

**Finding the Table:** The script finds the table containing company data by searching for all 'table' elements and selecting the second table (index 1).

**Extracting Table Headers:** It extracts the table headers by finding all 'th' elements within the table and strips any leading or trailing whitespaces from the text.

<img width="501" alt="image" src="https://github.com/Raezoxc/Web_Scraping_Data_-Python_Pandas/assets/153198226/3a337f52-69a8-47f3-a522-7a78d1293105">

<img width="509" alt="image" src="https://github.com/Raezoxc/Web_Scraping_Data_-Python_Pandas/assets/153198226/c8b09073-9cfa-47f3-a510-9be9d661c854">

**Creating an Empty DataFrame:** An empty Pandas DataFrame is created with column names extracted from the table headers.

**Parsing Table Data:** The script iterates through each row of the table (excluding the header row) and extracts the data from the 'td' elements. It then strips any leading or trailing whitespaces from the text and appends the row data to the DataFrame.

<img width="492" alt="image" src="https://github.com/Raezoxc/Web_Scraping_Data_-Python_Pandas/assets/153198226/1a28702b-1c2a-4ffa-b09d-53ee838e9797">

**Saving DataFrame as CSV:** Finally, the DataFrame is saved as a CSV file named 'Companies.csv' in the current working directory, with the index column omitted.

<img width="497" alt="image" src="https://github.com/Raezoxc/Web_Scraping_Data_-Python_Pandas/assets/153198226/852fb40d-6665-42f7-b50e-61240219fadb">

