
# Simple ETL Pipeline for Data Analysis using Python and SQL

This project implements an ETL (Extract, Transform, Load) pipeline for retail order data analysis using Python and SQL.

# Prerequisites
- Python
- Jupyter Notebook
- MySQL database
- Kaggle account and API credentials

# Installation
Install the required Python libraries as mentioned in the given Notebook as well as set up your Kaggle API credentials to download datasets.

To use Kaggle's beta API in order to interact with Datasets and download data, please follow the following steps:
 - Visit www.kaggle.com and sign in.
- Click on your account icon and select sittings
- Scroll down to API and click on the Create New Token
- A file kaggle.json will be downloaded. Copy the file and go to home directory (~/.kaggle/kaggle.json). Look for .kaggle folder and paste the downloaded (kaggle.json) file there.
In my case, the folder is: C:\Users\bilal\.kaggle\kaggle.json

# Usage
 1. Download the dataset: !kaggle datasets download ankitbansal06/retail-orders -f orders.csv
 2. #### Extraction (E): 
 - Extract the CSV file from the zip archive and load the data into a pandas DataFrame 
3. #### Transformation (T): 
- Perform data cleaning and transformation like handling null values, changing field names, calculations, changing field types etc.
4. #### Load (L):
- Make the connection and Load the data into a MySQL database:

    engine = create_engine('mysql+mysqlconnector://username:password@host:port/database')
-  Change the username, password, host, port number and database name according to your own credentials.

# Project Structure
- ETL-pipeline-data-analysis+sql.ipynb: Main script containing the ETL process
- orders.csv.zip: Downloaded zip file from Kaggle via API
- orders.csv: Raw data file (after extraction)
- SQL_Queries.txt: Basic SQL queries for data analysis
- README.md: This file which contain all necessary info about the project

# Data Source
The dataset used in this project is the "Retail Orders" dataset from Kaggle:
- Dataset URL: https://www.kaggle.com/datasets/ankitbansal06/retail-orders
