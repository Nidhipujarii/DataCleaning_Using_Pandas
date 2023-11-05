# Customer List Cleansing for Call Initiatives
## Overview
This project is designed to process and cleanse a customer list dataset. The primary goal is to prepare a dataset that can be used for calling initiatives by excluding any customers who have expressed a preference not to be contacted.
## Data Cleaning Process
The script executes a STEPS of data cleaning operations to prepare the dataset for the client's calling initiatives:

**1. Remove Duplicates**: Initiates the cleaning process by removing any duplicate entries in the dataset to ensure data integrity.

**2. Column Management**: Drops columns deemed not useful for the calling initiative, streamlining the dataset.

**3. Last_Name Cleaning**: Utilizes the strip function to remove unwanted characters from the last_name column, addressing elements on both sides of the string.

**4. Phone Number Standardization**: Formats the Phone_Numbers column by removing extraneous characters and standardizing the format to "000-000-0000".

**5. Error Handling**: Converts the Phone_Numbers column to a string data type to handle non-numeric values and ensure consistent formatting. After addressing the TypeError, the following formatting steps are taken:

  ***- String Conversion***: Every entry in the Phone_Numbers column is explicitly converted to a string to standardize the data type.
  
  ***- Formatting Numbers***: The phone numbers are then formatted to adhere to the standard "000-000-0000" format for consistency and readability.
  
  ***- Cleaning Placeholders***: Any placeholder strings such as 'nan' or 'Na' resulting from missing data are removed to clean up the phone number entries.
  
**6. Address Splitting**: Cleans the Address column by splitting it into three distinct columns: Street_address, State, and Zip_code.

**7. Column Formatting**: Formats the Paying customer and Do not contact columns for better clarity and utility in the dataset.

**8. Null Management**: Treats null values to maintain the dataset's completeness.

**9. Opt-out Filtering**: Removes details of customers who opted out in the Do_Not_Contact column.

**10. Incomplete Data Handling**: Excludes customer details lacking phone numbers.

**11. Index Resetting**: Resets the DataFrame index for orderly data.

**12. Final Clean-Up**: Drops the old 'Address' and 'zip code' columns post-extraction of necessary information.

## Output
The script produces a cleansed dataset, which now includes a list of customers who are open to future calls and suitable for the client's outreach efforts.

