# Data cleaning

## Drop unnecessary columns
- Q120 - empty question in schema filled with one unique value without nulls, possibly consent to processing data.
- SurveyLength, SurveyEase question about the respondent's feelings after completing the survey may be omitted.
## Remove duplicate and Incomplete Cases
- Removing rows where more than 60% of columns are null
- There isn't any duplicates
## Threat null values
- For now: nulls in columns of object type are replaced by 'NA' which means Not available/Not answered
## Handle data types
- ToDO - most importantly check columns with numeric values
## Remove nonsense Answers and Unreadable data
- CodingActivities was checked because of possibility of taking user inputs, but their answers aren't mentioned in data
- LearnCode the same as above
- LearnCodeOnline - column contains one extra value which is not mentioned in possible answers of pdf version of survey: "Formal documentation provided by the owner of the tech". Additionally nonsense answer which is "Click to write Choice 20". Like above user inputs are trimmed.
- LearnCodeCoursesCert as above, user inputs trimmed
- CompTotal - the question is answered by user input which lead to some unreal answers

## Remove outliers