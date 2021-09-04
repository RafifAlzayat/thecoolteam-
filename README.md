# Covid Analysis
## 9/3 Update
### Built upon the code that Alan created for the data processing. Specifically, I added back in the ethnicity column to our dataframe and instead took out the symptom and underlying conditions columns. This ended up leaving us with 6,952,336 rows of data instead of the 972,599 rows that were left when the data included the symptom and underlying conditions columns and then dropped the "NA" values from those columns. Therefore, this tells us that the underlying conditions and symptom columns have a lot of null values, and therefore would not be worth including in our analysis. 
## Data Topic and Overview
### Our team has chosen to analyze covid data from the CDC. We selected this data due to its relevancy as well as availability. The data has approximately 26 million rows, with each row being a unique individual that has been tested for covid. It includes the individuals age, race, ethnicity, hospitalization status, state, etc. We'd like to analyze and figure out which factor in the data contributes the most to an individual being hospitalized. 

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
  

