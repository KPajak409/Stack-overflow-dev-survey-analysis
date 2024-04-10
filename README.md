# Data cleaning

## Drop unnecessary columns
- Q120 - empty question in schema filled with one unique value without nulls, possibly consent to processing data
- 
## Remove duplicate and Incomplete Cases
## Threat null values
## Handle data types
## Remove outliers

## Remove nonsense Answers and Unreadable data
- CodingActivities was checked because of possibility of taking user inputs, but their answers aren't mentioned in data
- LearnCode the same as above
- LearnCodeOnline - column contains one extra value which is not mentioned in possible answers of pdf version of survey: "Formal documentation provided by the owner of the tech". Additionally nonsense answer which is "Click to write Choice 20". Like above user inputs are trimmed.
- LearnCodeCoursesCert as above, user inputs trimmed