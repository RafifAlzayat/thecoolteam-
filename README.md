# Covid Analysis

## AWS DB
We are using a postgresql on AWS; to access the db use the following:

AWS URL: database-1.cvyxzrizmaqm.us-east-1.rds.amazonaws.com

Port: 5432

DB name: postgres

Schema: finalProject

Username: [ask rafif]

Password: [ask rafif]

## DATA TABLE CREATION
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
## DATA LOAD

We load the data found here:

https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data-with-Ge/n8mc-b4w4/data

