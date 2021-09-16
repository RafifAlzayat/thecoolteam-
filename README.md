# alan-branch


### Resources
**Source of Data** : https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://data.cdc.gov/resource/n8mc-b4w4.json, https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://rafifcoviddata.s3.amazonaws.com/COVID-19_Case_Surveillance_Public_Use_Data_with_Geography.csv

Json Data info: 19 columns, 28,652,764 rows. 

## Overview and Timeline of Project

### Write up on the Machine Learning
Description of preliminary data preprocessing
Description of preliminary feature engineering and preliminary feature selection, including their decision-making process
Description of how data was split into training and testing sets
Explanation of model choice, including limitations and benefits
Models: 

- BalancedRandomForestClassifier
- EasyEnsembleClassifier
- LogisticRegression
- DecisionTreeClassifier
- GradientBoostingClassifier
- RandomOverSampler
- SMOTE




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
