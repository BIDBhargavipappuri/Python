# PAN Number Validation Project uisng Regex

Data Cleaning and Validation-

Objective:

You are tasked with cleaning and validating a dataset containing the Permanent Account Numbers (PAN) of Indian nationals. The goal is to ensure that each PAN number adheres to the official format and is categorised as either Valid or Invalid. The dataset is given in a separate Excel file.

PAN Number Validation Dataset.xlsx(its stored on my desktop)

Instructions:

Data Cleaning and Preprocessing
   
  1. Identify and handle missing data
     
    - PAN numbers may have missing values.
       
    - Handle them appropriately by removing rows or imputing values.

  2. Check for duplicates
     
    - Ensure there are no duplicate PAN numbers.
     
    - Remove duplicates if found.

 3.  Handle leading/trailing spaces
   
    - PAN numbers may contain extra spaces.
     
    - Remove any leading or trailing spaces.

 4.  Correct letter case
   
    - Ensure all PAN numbers are in uppercase.
     
    - Convert lowercase letters to uppercase.

PAN Format Validation

 1.  Length requirement
   
    - PAN must be exactly 10 characters long.

 2.  Overall structure
    
    - Correct Format: AAAAA1234A. 

 3.  First five characters (alphabets)
    
    - Must be uppercase alphabetic characters.
    
    - Adjacent characters cannot be the same (e.g., AABCD is invalid; AXBCD is valid).
     
    - All five characters cannot form a sequence (e.g., ABCDE, BCDEF are invalid; ABCDX is valid).

 4.  Next four characters (digits)
    
    - Must be numeric digits.
    
    - Adjacent digits cannot be the same (e.g., 1123 is invalid; 1923 is valid).
    
    - All four digits cannot form a sequence (e.g., 1234, 2345 are invalid).

5.   Last character
   
    - Must be an uppercase alphabetic character.

6.   Example
   
    - Example of a valid PAN: AHGVE1276F

Categorisation

 1.  Valid PAN
   
    - Matches the complete PAN format.

 2.  Invalid PAN
    
    - Does not match the format, incomplete, or contains non‑alphanumeric characters.

Tasks

 1.  Validate PAN numbers based on the above rules.
   
 2.   Create two categories:
   
     - Valid PAN

     - Invalid PAN

Summary Report

  1. Total records processed
 
  2. Total valid PANs
  
  3. Total invalid PANs
 
  4. Total missing or incomplete PANs (if applicable)
