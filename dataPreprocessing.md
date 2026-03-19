
### Data Preprocessing

We start by importing the raw data. This includes the digital data and the old paper data from the satisfaction customer database. We also import the raw data from the course, student, student admission and the study program.

#### Preprocessing the digital and paper data

We do a seperate preprocessing step for the digital data and the paper data.
For the paper data we:

1. Combine the date and slot1/slot2 into one column Timestamp.
2. Create individual row for each visitor in the paper data. We have to do this because the paper data has multiple visitors in one row, and we want to have one row per visitor for our analysis.

We then rename the columns in the paper data and the digital data to so we can combine.

#### Preprocessing the course, student and study program data

We clean and rename the dtu data (Course DB, Student DB, study program DB) such that the information is consistent across the different data sources.

In the student data missing values are filled as "other" for both the gender and education name (BEng, BSc, MSc).

For the study program some of the enrolled statistics are missing, so we fill those with 0 and convert the columns to numeric.

We then save the preprocessed data to the datalakehouse under tables and PreProcessedData.
