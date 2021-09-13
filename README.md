# Covid Analysis

### Resources
**Raw Data Source** : https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://data.cdc.gov/resource/n8mc-b4w4.json, https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://rafifcoviddata.s3.amazonaws.com/COVID-19_Case_Surveillance_Public_Use_Data_with_Geography.csv

Json Data info: 19 columns, 28,652,764 rows. 

**Google Slides Link:** https://docs.google.com/presentation/d/16uZDT7L-L3IMNzPAzESrh303vs9Um8ul3L3JFFOzpnk/edit?usp=sharing

## Data Topic and Overview
Our team has chosen to analyze covid data from the CDC. We selected this data due to its relevancy as well as availability. The data has approximately 26 million rows, with each row being a unique individual that has been tested for covid. It includes the individuals age, race, ethnicity, hospitalization status, state, etc. We'd like to analyze and figure out which factor in the data contributes the most to an individual being hospitalized. 

Ava to add: 
✓ Description of the data exploration phase of the project 
✓ Description of the analysis phase of the project

## Machine Learning Models

Because all of our data is either ordinal or classificatin data we will have to change our data into numbers via dummy variables. We can use the following models and see which model like best or which models are better for visualizing different conclusions:
  
  * Linear Least Squares
  * Ridge Regression
  * Lasso
  * Multinomial Logistic Regression
  * Linear Support Vector Machines (SVMs)
  * Random Forest
  * Gradient-Boosted Tree (GBT)
  * One vs. Rest
  * Naive Bayes
  * Factorization Machine Classifier

We will create each one of these models with our COVID-19 data, and tweak the parameters to test for under fitting or over fitting, to figure out which models and at what parameters are best for visualizing certain conclusions about the data. All of our models will be supervized machine learning models.
  
We can use SVMs, decision trees, random forest, gradient boosted trees, and naive Bayes models to solve binary problems like who is likely to contract COVID-19. We can use decision trees, random forest, and naive Bayes multiclass classification problems. We can use decision trees, random forest, linear least squares, ridge regression, Lasso, multinomial logistic regression, and GBT to visualize regressions.

Ryan/Alan to add: 
✓ Description of preliminary data preprocessing 
✓ Description of preliminary feature engineering and preliminary feature selection, including their decision-making process 
✓ Description of how data was split into training and testing sets 
✓ Explanation of model choice, including limitations and benefits
  
The diagram for the machine learning model is below: 
  ![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/main/Machine%20Learning%20Model%20Diagram.jpg)
  
 ## Database Information
 
### AWS DB
We are using a postgresql on AWS; to access the db use the following:

AWS URL: database-1.cvyxzrizmaqm.us-east-1.rds.amazonaws.com

Port: 5432

DB name: postgres

Schema: finalProject

Username: [ask rafif]

Password: [ask rafif]

Rafif to add: 
✓ Database stores static data for use during the project 
✓ Database interfaces with the project in some format (e.g., scraping updates the database, or database connects to the model) 
✓ Includes at least two tables (or collections, if using MongoDB) 
✓ Includes at least one join using the database language (not including any joins in Pandas) 
✓ Includes at least one connection string (using SQLAlchemy or PyMongo)
Note: If you use a SQL database, you must provide your ERD with relationships.

### DATA TABLE CREATION
To create the table we used the following SQL:
```
CREATE TABLE covid_data (
  case_month TEXT,
  res_state TEXT,
  state_fips_code TEXT,
  res_county TEXT,
  county_fips_code TEXT,
  age_group TEXT,
  sex TEXT,
  race TEXT,
  ethnicity TEXT,
  case_positive_specimen_interval TEXT,
  case_onset_interval TEXT,
  process TEXT,
  exposure_yn TEXT,
  current_status TEXT,
  symptom_status TEXT,
  hosp_yn TEXT,
  icu_yn TEXT,
  death_yn TEXT,
  underlying_conditions_yn TEXT
);
```
### DATA LOAD

We load the data found here:

https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data

![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/rafif-branch/resources/1.png)

![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/rafif-branch/resources/2.png)

![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/rafif-branch/resources/3.png)

## Cleaned Covid Data CSV File
S3 bucket URI to cleaned data: https://rafifcoviddata.s3.amazonaws.com/cleaned_covid_data.csv
![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/rafif-csvfile/resources/cleaned_data_sample.png)

## Dashboard
The dashboards created so far used Tableau public as the visualization tool. The interactive elements include real time filters to slice and update the visualizations to show covid data based on sex, race, ethnicity, age group, etc. 

### Covid Hospitalizations Dashboard 
Link to tableau public: https://public.tableau.com/app/profile/ava.wolfe/viz/CovidHospitalizationAnalysis/Hospitalizations?publish=yes
![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/ava-branch/Hospitalizations.png)

### Covid by State Per Capita Dashboard
![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/ava-branch/Map.png)


