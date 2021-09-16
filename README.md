# Covid Analysis

### Resources
**Raw Data Source** : https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://data.cdc.gov/resource/n8mc-b4w4.json, https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data, https://rafifcoviddata.s3.amazonaws.com/COVID-19_Case_Surveillance_Public_Use_Data_with_Geography.csv

Json Data info: 19 columns, 28,652,764 rows. 

**Prepped CSV File**: https://rafifcoviddata.s3.amazonaws.com/cleaned_covid_data.csv
![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/rafif-csvfile/resources/cleaned_data_sample.png)

**Google Slides Link:** https://docs.google.com/presentation/d/16uZDT7L-L3IMNzPAzESrh303vs9Um8ul3L3JFFOzpnk/edit?usp=sharing

## Data Overview

### Data Topic
Our team has chosen to analyze covid data from the CDC. We selected this data due to its relevancy as well as availability. The data has approximately 26 million rows, with each row being a unique individual that has been tested for covid. It includes the individuals age, race, ethnicity, hospitalization status, state, etc. We'd like to analyze and figure out which factor in the data contributes the most to an individual being hospitalized. After our data exploration, the team decided to decrease the size of the database and only analyze covid cases in the state of Virginia. 

### Data Exploration/Analysis
Data Preparation/Database Code: https://github.com/RafifAlzayat/thecoolteam-/blob/main/Code/Data_Prep.ipynb

Data Exploration Code: https://github.com/RafifAlzayat/thecoolteam-/blob/main/Code/Covid_Data_Exploration.ipynb

For the data exploration and analysis phase of our project, we first examined the null values in our data set. Then, we determined that even after getting rid of rows with null values, our dataset was still too large at ~7M rows to perform our machine learning models. From there, we decided to focus specifically on covid hopsitalizations in the state of Virginia. After filtering to only include Virginia data, we made pie charts for each of our factors to ensure that there was still a good distribution of data across all of the different factors. An example of a pie chart we created can be found below. 
#### Age Group Pie Chart
![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/main/Covid%20Analysis%20Images/Age%20Group%20Pie%20Chart.png)


## Machine Learning Models
Machine Learning Model Code: https://github.com/RafifAlzayat/thecoolteam-/blob/main/Code/Covid_Machine_Learning.ipynb
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

**Ryan/Alan to add:** 
✓ Description of preliminary data preprocessing 
✓ Description of preliminary feature engineering and preliminary feature selection, including their decision-making process 
✓ Description of how data was split into training and testing sets 
✓ Explanation of model choice, including limitations and benefits
  
The diagram for the machine learning model is below: 
  ![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/main/Covid%20Analysis%20Images/Machine%20Learning%20Model%20Diagram%20(1).jpg)
  
 ## Database Information
Data Prep/Database Code: https://github.com/RafifAlzayat/thecoolteam-/blob/main/Code/Data_Prep.ipynb
### AWS DB
We are using a postgresql on AWS; to access the db use the following:

AWS URL: database-1.cvyxzrizmaqm.us-east-1.rds.amazonaws.com

Port: 5432

DB name: postgres

Schema: Public

Username: [ask rafif]

Password: [ask rafif]

### ERD 
Below is the ERD for our database: 

![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/main/Covid%20Analysis%20Images/ERD.png)


### Cleaned Data Export
We wrote our full cleaned df including all U.S. states data from pyspark to our RDS, resulting in a "cleaned_covid_data" table in our RDS. 

![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/main/Covid%20Analysis%20Images/Cleaned%20Covid%20Data%20Table.png)

### Join
We wrote our virginia df from pyspark to our RDS, resulting in a "virginia_covid_data" table in our RDS. We did the same thing for our VA county population dataset, resulting in a "county_population" table in our RDS. From there, we used SGLAlchemy to join the two tables together. 


#### Joined Table
![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/main/Covid%20Analysis%20Images/Joined%20Table.png)


## Dashboard
The dashboards created so far used Tableau public as the visualization tool. The interactive elements include real time filters to slice and update the visualizations to show covid data based on sex, race, ethnicity, age group, etc. Draft storyboard for full dashboard can be found on our google slides here: **Google Slides Link:** https://docs.google.com/presentation/d/16uZDT7L-L3IMNzPAzESrh303vs9Um8ul3L3JFFOzpnk/edit?usp=sharing

Link to tableau public: https://public.tableau.com/app/profile/ava.wolfe/viz/CovidHospitalizationAnalysis/Hospitalizations?publish=yes

### VA Covid Hospitalizations Dashboard 
![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/main/Covid%20Analysis%20Images/Hospitalizations%20Dashboard.png)

### Covid by VA County Per Capita Dashboard
![alt text](https://github.com/RafifAlzayat/thecoolteam-/blob/main/Covid%20Analysis%20Images/County%20Map.png)


