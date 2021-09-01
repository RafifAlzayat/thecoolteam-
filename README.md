# Covid Analysis

## DATA TABLE CREATION
We are using a postgresql on AWS. To create the table we used the following SQL:

```
CREATE TABLE covid_data (
  id TEXT PRIMARY KEY NOT NULL,
  case_month DATE,
  res_state TEXT,
  state_fips_code TEXT,
  res_county TEXT,
  county_fips_code TEXT,
  age_group TEXT,
  sex TEXT,
  race TEXT,
  ethnicity TEXT,
  case_positive_specimen_interval Boolean,
  case_onset_interval Boolean,
  process TEXT,
  exposure_yn TEXT,
  current_status TEXT,
  symptom_status TEXT,
  hosp_yn TEXT,
  icu_yn TEXT,
  death_yn TEXT,
  underlying_conditions_yn text
);
```


