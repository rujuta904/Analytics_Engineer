Documentation: Housing Data Cleaning and Analysis

Data Sources:

Imported four CSV files: inventory_data.csv, majors_data.csv, occupancy_data.csv, and persons_data.csv.

Data Cleaning and Validation:
a) Inventory Data (df_inventory):

Removed duplicates and rows with missing values.
Validated room and bed naming conventions.
Ensured uniqueness of bedId.

b) Majors Data (df_majors):

Handled duplicates, keeping the most recent entry.
Standardized text fields.
Ensured uniqueness of id and displayId.

c) Occupancy Data (df_occupancy):

Handled missing values and duplicates.
Standardized text fields.

d) Persons Data (df_persons):

Handled duplicate emails, keeping the most recent entry.
Validated email addresses, dates of birth, and state abbreviations.
Standardized names and addresses.
Split address into multiple columns.


Data Merging and Transformation:

Created df_occupancy_inventory by merging occupancy and inventory data.
Created df_majors_persons linking students to their majors.
Combined all dataframes to create a final output (df_combined).


Key Assumptions:

For duplicate entries, the most recent data is assumed to be correct.
Email addresses must be unique for each person.
Addresses follow a consistent format: street, city, state.
All states are represented by standard two-letter abbreviations.
Majors are comma-separated strings in the persons data.


Final Output:

Created df_final by removing rows with missing bedId values.
Retained a separate df_missing_bedId for records without bed assignments.


Data Integrity:

Ensured no missing values in critical fields (e.g., personId, email, majorIds).
Validated data types and formats throughout the process.


This process cleaned and standardized the data, handling inconsistencies and missing values, to create 
a unified dataset suitable for further analysis.
