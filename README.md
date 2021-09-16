# alan-branch


### Resources
**Source of Data** : https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://data.cdc.gov/resource/n8mc-b4w4.json, https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://rafifcoviddata.s3.amazonaws.com/COVID-19_Case_Surveillance_Public_Use_Data_with_Geography.csv

Json Data info: 19 columns, 28,652,764 rows. 

## Overview and Timeline of Project

### Write up on the Machine Learning
The data was in JSON format directly from the CDC website and we loaded the raw data into an AWS RDS which allowed us to make a preliminary dataset using postgres in pgAdmin. The data was then loaded into a csv file using an S3 bucket which can then be loaded into pyspark for cleaning. The data was cleaned to drop null values as well as columns that weren’t essential. The cleaned table data included variables from every state in the United States which we could draw from if we wished to split off into different states. The decision was made to split the dataset further into individual states for a more efficient machine learning process, so the sample state of Virginia was selected. The data was split with a target of “hosp_yn” which was the column that detailed if the patient went to the hospital. A dummy dataset was created without  “hosp_yn” which allowed us to split the data into training and testing sets. The models we decided to use were: 

- BalancedRandomForestClassifier
  - The BalancedRandomForestClassifier has a balanced accuracy score of 78%
- EasyEnsembleClassifier
-   The Easy Ensemble AdaBoost Classifier has a balanced accuracy score of 75%
- LogisticRegression
-   The LogisticRegression has a balanced accuracy score of 75%
- DecisionTreeClassifier
-   The DecisionTreeClassifier has a balanced accuracy score of 93%
- GradientBoostingClassifier
-   The GradientBoostingClassifier has a balanced accuracy score of 93%
- RandomOverSampler
-   The RandomOverSampler has a balanced accuracy score of just over 75% 
- SMOTE
-   The SMOTE Oversampling has a balanced accuracy score of 75% 




### Update 09/13/2021
We as a group have pivoted to separating the data even further by state as this will give us the necessary leeway to run the data in pandas for the supervised machine learning portion. Separating the data by state also accomplishes much in respect to the data exploratory phase as we will need to figure out what the data means and how to utilize the joins table we have from Ryan's branch. I have successfully imported the Logistic Regression models of RandomOverSampler and SMOTE in the resampling files. BalancedRandomForestClassifier and EasyEnsembleClassifier are in the CovidDataEnsemble data file. Both states are separated by their abbreviation names on the files VA and CT. 



### Update 09/08/2021
Threw in the cleaned covid csv file into jupyter notebook and split the data to test and train them. As it turns out the data is too massive to be handled in a pandas so therefore we would have to try writing them on pyspark on google colab, if that doesn't work then we'll try something else. I have written the two codes of Resampling and Ensemble as if they would be written in a Jupyter notebook as a framework of what we need to do on google colab. So there's that. The cleaned csv that took so long works perfectly tho, big ups. At least we can keep everything in one big google collab file in the preliminary database.


### Update 09/01/2021
The database was pulled from the cdc website onto an rds and converted from json format to a dataframe using SQL, the SQL data frame was then refactored into a csv format and put again onto a s3 bucket to put onto pyspark. 
Through pyspark the preliminary data frame was created after dropping unnecessary columns and taking out rows that had Missing, Unknown, NA, or null values. This left the data frame with 8 columns and 972599 rows as opposed to the original 19 columns and 28,652,764 rows.

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
