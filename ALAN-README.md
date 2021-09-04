# alan-branch


### Resources
**Source of Data** : https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://data.cdc.gov/resource/n8mc-b4w4.json, https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://rafifcoviddata.s3.amazonaws.com/COVID-19_Case_Surveillance_Public_Use_Data_with_Geography.csv

Json Data info: 19 columns, 28,652,764 rows. 

## Overview and Timeline of Project



### Update 09/01/2021
The database was pulled from the cdc website onto an rds and converted from json format to a dataframe using SQL, the SQL dataframe was then refactored into a cvs format and put again onto a s3 bucket to put onto pyspark. 
Through pyspark the preliminary dataframe was created after dropping unneccacry columns and taking out rows that had Missing, Unknown, NA, or null values. This left the dataframe with 8 columns and 972599 rows as oppsoed to the orginal 19 columns and 28,652,764 rows.
To do note:
- the environmental variable still needs to be stored 
- dummy varables still need to be created 
- still need to Configure settings for RDS
- write the dataframe into rds
- and finally implment machine learning models.




### Update 08/30/2021
This is the branch Alan Fanng will push into. His first assingment is to create the provisional database that stands in for the final database, it mus accomplish the following: 
- Sample data that mimics the expected final database structure or schema
- Draft machine learning module is connected to the provisional database

Change notes: 
- Kernal was changed from PythonData to mlev to be abale to run RandomForest and other supervised machine learning samples.
- Json file was added in

To Do Notes:
- Clean the dataframe to only the columns we need.
- Figure out the expected final database schema.
- Figure out how to connect machine leaning module to this database.
