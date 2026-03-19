# Azure Blob Storage to Local SQL Server Using Python- 

#  Objective

To design and implement an end‑to‑end ETL pipeline that extracts public NYC Taxi trip data from Azure Blob Storage, processes and transforms it using Python, and loads the curated dataset into a local SQL Server database for analytics and reporting. 

This project demonstrates cloud‑to‑on‑premise data integration, data transformation using Pandas, and database loading using SQLAlchemy and PyODBC.

Highlights:

- Cloud ingestion (Azure Blob Storage)
  
- Python transformation (Pandas)
  
- Local SQL Server loading
  
- ETL pipeline design
  
- Real‑world dataset
  
- Analytics readiness

  #  Processing Steps

  **Read Parquet files from Blob**
  
   - Use `pandas.read_parquet()` with the HTTPS URL of the Parquet file.
   - Verify:
     - Data loads successfully.
     - Row and column counts look reasonable.

 **Data cleaning and preprocessing**  

  1) Select relevant columns
     
   - Keep only the columns needed for analysis (e.g., pickup, dropoff, distance, fare, tip).

  2) Handle missing and invalid data
     
   - Drop rows with critical missing values (e.g., timestamps, fare).
     
   - Remove duplicates.
     
   - Filter out invalid values (negative or zero distance/fare).

  3). Standardise data types
  
   - Ensure datetime columns are proper `datetime` type.
     
   - Ensure numeric columns are `int`/`float` as needed.
    
  

