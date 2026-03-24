# Azure Blob Storage to Local SQL Server Using Python- 

#  Objective

To design and implement an end‑to‑end ETL pipeline that extracts public NYC Taxi trip data from Azure Blob Storage, processes and transforms it using Python, and loads the curated dataset into a local SQL Server database for analytics and reporting. 

This project demonstrates cloud‑to‑on‑premise data integration, data transformation using Pandas, and database loading using SQLAlchemy and PyODBC.

Highlights:

- Cloud extraction (Azure Blob Storage)
  
- Python transformation (Pandas)
  
- Local SQL Server loading
  
- ETL pipeline design
  
- Real‑world dataset
  
- Analytics readiness


# Pandas cannot read a folder

Pandas needs:

- a specific file name
  
- a direct file path
  
If the folder contains multiple files or no CSV, Pandas fails with 404.

So we will:

use direct URL to access , as it it public blob here is the URL ( data set of NYC Taxi public dataset).

https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2019-01.parquet 


#  Processing Steps

**Read Parquet files from Blob**
  
   1) Use Python functions with the HTTPS URL to read the Parquet file - 
   
     - Identifying the correct libraries
     - Verifying the connection
     - Loading the Parquet file
     - Checking row/column counts


 **Data cleaning and preprocessing**  

  1) Select relevant columns

    - pickup datetime,dropoff datetime,passenger count,trip distance,fare amount,tip amount,total amount.


  2) Handle missing and invalid data
     
    - Drop rows with critical missing values (- pickup/dropoff timestamp,- fare amount- Zero).
     
    - Remove duplicates.
     
    - Filter out invalid values (negative or zero distance/fare).

  3) Standardise data types
  
    - Ensure datetime columns are proper `datetime` type.
     
    - Ensure numeric columns are `int`/`float` as needed.

 **Data transformation**  
  
  1) Create derived fields
 
    - trip duration in minutes using pickup and dropoff timestamps.
    
    - Categorise trips (Short / Medium / Long).
     
    - Rename columns for consistency.

    
 **Create Table in SQL to insert data from blob**  

    - Original fields
    
    - Cleaned numeric fields
    
    - Derived fields (trip_duration_minutes, trip_category


 **Load cleaned data into SQL Server**  
 
 1)  Establish SQL Server connection
 
    - Use SQLAlchemy + PyODBC to connect to your local SQL Server instance.
    
    - Load DataFrame into SQL table
    
    - Use df.to_sql() to insert data into the target table.
    
    - Use batch inserts (chunksize) for performance.
    
    - Validate load
    
    - Check row counts in SQL Server.
    
    - Confirm schema and data types.


