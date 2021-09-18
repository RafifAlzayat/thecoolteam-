# Using Machine Learning to Predict Hospitalization for COVID-19

## Overview

  We will be using COVID-19 data from the Center for Disease Control (CDC) to predict the likelihood of some being hospitalized for COVID-19 in Virginia and Connecticut and then to compare the two. Our machine learning models' target is whether of not someone gets hospitalized and they will consider the following features:
  
  * Resident's state
  * Resident's county
  * Age group (0 - 17, 18 - 49, 50 - 64, 64+)
  * Sex (Female, Male)
  * Race (American Indian/Alaska Native, Asian, Black, Multiple/Other, Native Hawaiian/Other Pacific Islander, White)
  * Ethnicity (Hispanic/Latino, Non-Hispanic/Latino)

  Because all of our data is either ordinal or classificatin data we will have to change our data into numbers via dummy variables. We can use the following models and see which model like best or which models are better for visualizing different conclusions:
  
  * BalancedRandomForestClassifier
  * EasyEnsembleClassifier
  * LogisticRegression
  * GradientBoostingClassifier
  * DecisionTreeClassifier
  * RandomOverSampler
  * SMOTE
  * Deep Learning

  We will create each one of these models with our COVID-19 data, and tweak the parameters to test for under fitting or over fitting, to figure out which models and at what parameters are best for visualizing certain conclusions about the data. We will be using supervised machine learning models and a deep learning model
  
  We can use SVMs, decision trees, random forest, GBT, and naive Bayes models to solve binary problems like who is likely to contract COVID-19. We can use decision trees, random forest, and naive Bayes multiclass classification problems. We can use decision trees, random forest, multinomial logistic regression, and GBT to visualize regressions.
  

## Machine Learning Models

### Logistic Regression, RandomOverSampler, and SMOTE for CT
  * File name: CT_1_CovidDataResampling.ipynb
#### Process
#### Results
#### Benefits and Limitations

### BalancedRandomForestClassifier and EasyEnsembleClassifier for CT
  * File name: CT_2_CovidDataEnsemble.ipynb
#### Process
  1. Import Libraries.
  2. Read csv file.
  3. Split the data:
    * Using the train_test_split function from sklearn
  5. Create features and target.
  6. Train the model:
    * Using the BalancedRandomForestClassifier from imblearn
  7. Create a confusion matrix imbalanced classification report to check accuracy.
  8. List features in order of importance
  9. Train the EasyEnsembleClassifier:
    * Using the EasyEnsembleClassifier from imblearn
  10.Create a confusion matrix imbalanced classification report to check accuracy.
#### Results
##### Top 10 Features
  1. Age 65+
  2. Age 18 - 49
  3. Age 50 - 64
  4. Age 0 - 17
  5. New Haven
  6. Tolland
  7. Hartford
  8. Male
  9. Female
  10. Black
#### Benefits and Limitations

### Deep Learning for CT
#### Process
#### Results
#### Benefits and Limitations

### LogisticRegression, RandomOverSampler, and SMOTE for VA
   * File name: VA_1_CovidDataResmapling.ipynb
#### Process
#### Results
#### Benefits and Limitations

### BalancedRandomForestClassifier and EasyEnsembleClassifier for VA
  * File name: VA_2_CovidDataEnsemble.ipynb
#### Process
  1. Import Libraries.
  2. Read csv file.
  3. Split the data:
    * Using the train_test_split function from sklearn
  5. Create features and target.
  6. Train the model:
    * Using the BalancedRandomForestClassifier from imblearn
  7. Create a confusion matrix imbalanced classification report to check accuracy.
  8. List features in order of importance
  9. Train the EasyEnsembleClassifier:
    * Using the EasyEnsembleClassifier from imblearn
  10.Create a confusion matrix imbalanced classification report to check accuracy.
#### Results
##### Top 10 Features
  1. Age 65+
  2. Age 18 - 49
  3. Age 0 - 17
  4. Age 50 - 64
  5. Black
  6. White
  7. Male 
  8. Female
  9. Hispanic/Latino
  10. Fairfax
#### Benefits and Limitations

### Deep Learning for VA
#### Process
#### Results
#### Benefits and Limitations
