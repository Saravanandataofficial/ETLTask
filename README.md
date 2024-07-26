# ETLTask
ETL process that involves extracting data from a CSV file, transforming this data, and loading it into a SQL Server production table via a staging table

Step 1 --- To Load the CSV file using flatfile source,  I have used the text qualifier field in flat file connection to remove the string qualifiers. 
           1- Load CSV File
           2 - Remove Text Qualifiers
           3 - Filter Errors
           3a - Set Data Types  or 3b - Error Data
           5 - Remove Duplicates
           6 - Load to Stage
Step 2 --- Stage to Production -- have implemented SCD type2 with Lookup and conditional split
           1 - Stage Source
           2 - Lookup
           3a - Lookup No Match - UPDATE Date and LOAD New Records
           3b - Lookup Match - CHECK if Data Changes and UPDATE if Data changes
