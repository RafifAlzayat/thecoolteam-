# Covid Analysis
## 9/3 Update
### Built upon the code that Alan created for the data processing. Specifically, I added back in the ethnicity column to our dataframe and instead took out the symptom and underlying conditions columns. This ended up leaving us with 6,952,336 rows of data instead of the 972,599 rows that were left when the data included the symptom and underlying conditions columns and then dropped the "NA" values from those columns. Therefore, this tells us that the underlying conditions and symptom columns have a lot of null values, and therefore would not be worth including in our analysis. 
## Data Topic and Overview
### Our team has chosen to analyze covid data from the CDC. We selected this data due to its relevancy as well as availability. The data has approximately 26 million rows, with each row being a unique individual that has been tested for covid. It includes the individuals age, race, ethnicity, hospitalization status, state, etc. We'd like to analyze and figure out which factor in the data contributes the most to an individual being hospitalized. 
