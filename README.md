# Covid Analysis

### Resources
**Source of Data** : https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://data.cdc.gov/resource/n8mc-b4w4.json, https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://rafifcoviddata.s3.amazonaws.com/COVID-19_Case_Surveillance_Public_Use_Data_with_Geography.csv

Json Data info: 19 columns, 28,652,764 rows. 

### 9/3 Update
Built upon the code that Alan created for the data processing. Specifically, I added back in the ethnicity column to our dataframe and instead took out the symptom and underlying conditions columns. This ended up leaving us with 6,952,336 rows of data instead of the 972,599 rows that were left when the data included the symptom and underlying conditions columns and then dropped the "NA" values from those columns. Therefore, this tells us that the underlying conditions and symptom columns have a lot of null values, and therefore would not be worth including in our analysis. 

### Update 09/01/2021
The database was pulled from the cdc website onto an rds and converted from json format to a dataframe using SQL, the SQL dataframe was then refactored into a cvs format and put again onto a s3 bucket to put onto pyspark. 
Through pyspark the preliminary dataframe was created after dropping unneccacry columns and taking out rows that had Missing, Unknown, NA, or null values. This left the dataframe with 8 columns and 972599 rows as oppsoed to the orginal 19 columns and 28,652,764 rows.



## Data Topic and Overview
 Our team has chosen to analyze covid data from the CDC. We selected this data due to its relevancy as well as availability. The data has approximately 26 million rows, with each row being a unique individual that has been tested for covid. It includes the individuals age, race, ethnicity, hospitalization status, state, etc. We'd like to analyze and figure out which factor in the data contributes the most to an individual being hospitalized. 
