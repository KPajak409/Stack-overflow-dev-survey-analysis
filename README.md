# Data source
Data utilized in this project comes from widely accesible source i.e [Stack Overflow site](https://insights.stackoverflow.com/survey/). It is annual developer survey performed by Stack Overflow, which is the best known Q&A platform that millions of people visit every month to ask questions, learn, and share technical knowledge. The questions asked each year are selected accordingly to raising trends in Information Technology area and due to it's dynamically changing nature they may differ significantly every year.
## Objectives
This project is going to analyze data from survey taken in 2023. Stack Overflow has already done [analysis](https://survey.stackoverflow.co/2023/) on this survey, but there lays more valuable informations inside this data, which can be obtained with help of visualization.
\
Questions that i would like to answer through analysis of this data:
- Does people age affect their likeliness of using AI?
- Does people who use AI earning more?
- How much does remote working matter to employees?
- How does coding experience affect the level of pay?
- What are the most popular technologies used in Poland?
- Are you more likely to get a job as a developer if you have a master's degree?

Because of where I live, it will be extremely interesting to analyze only my region and the possibility to compare it with the rest of the world. This would help to draw conclusions about actual situation at the local job market and position it situation among the rest.

## Structure
Data is placed in two files in csv format. 
- Schema contains information about questions itself, like: question name, content, is it forced to answer, type.
- Public contains information about user answers. Each row corrensponds to single person given answers and each column corrensponds to answer to specific questions. In this data there is most of possible types of values stored in columns, like: categorical, numeric, categorical list, intervals.

# Data cleaning

## Drop unnecessary columns
- Q120 - empty question in schema filled with one unique value without nulls, possibly consent to processing data.
- SurveyLength, SurveyEase question about the respondent's feelings after completing the survey may be omitted.
- SOAI long strings containing user opinions about AI, great for NLP, not particularly for this project.
- YearsCodePro - a lot of nulls to handle, very similar to previous YearsCode. The only difference is this question doesn't include coding years during education.
## Remove duplicate and Incomplete Cases
- Removing rows where more than 60% of columns are null.
- There isn't any duplicates.
## Threat null values
- For now: nulls in columns containing text data, are replaced by 'NA' which means Not available/Not answered.
- YearsCode - removed rows with nulls.
## Handle data types
- YearsCode - categorized from integer values
## Remove nonsense Answers and Unreadable data
- Most of questions that allows user input doesn't contain this information in data. Only SOAI column contains user inputs.
- LearnCodeOnline - column contains one extra value which is not mentioned in possible answers of pdf version of survey: "Formal documentation provided by the owner of the tech". Additionally nonsense answer which is "Click to write Choice 20". Like above user inputs are trimmed.
- CompTotal - the question is answered by the user through input, leading to unrealistic answers. Rows with CompTotal above $1 million are removed to get rid of outliers and reduce the influence of high earners on further analysis.

## Remove outliers

## Columns name - dtype; isDone; operations
ResponseId - integer unique ✅ checked <br>
Q120 - string ✅ removed <br>
MainBranch - categorical ✅ checked<br>
Age - categorical ✅ checked<br>
Employment - categorical list ✅ <br>
RemoteWork - categorical ✅ nulls replaced <br>
CodingActivities ✅ checked input answers <br> 
EdLevel - categorical ✅ checked <br> 
LearnCode - categorical✅ checked input answers <br>
LearnCodeOnline - categorical✅ checked input answers <br>
LearnCodeCoursesCert - categorical ✅ checked input answers <br>
YearsCode - categorical ✅ remove nulls, convert to intervals <br>
YearsCodePro - categorical ✅ removed <br>
DevType - categorical ✅ checked input answers <br>
OrgSize - categorical ✅ nulls replaced <br>
PurchaseInfluence - categorical ✅ checked <br>
TechList - categorical ✅ checked input answers <br>
BuyNewTool - categorical list ✅ checked input answers <br>
Country - categorical ✅ <br>
Currency - categorical ✅ <br>
CompTotal integer ✅ casted to int, removed unreal values <br>
LanguageHaveWorkedWith - categorical list ✅ checked input answers <br>
LanguageWantToWorkWith - categorical list ✅ user inputs check omitted <br>
DatabaseHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
DatabaseWantToWorkWith - categorical list ✅ user inputs check omitted <br>
PlatformHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
PlatformWantToWorkWith - categorical list ✅ user inputs check omitted <br>
WebframeHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
WebframeWantToWorkWith - categorical list ✅ user inputs check omitted <br>
MiscTechHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
MiscTechWantToWorkWith - categorical list ✅ user inputs check omitted <br>
ToolsTechHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
ToolsTechWantToWorkWith - categorical list ✅ user inputs check omitted <br>
NEWCollabToolsHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
NEWCollabToolsWantToWorkWith - categorical list ✅ user inputs check omitted <br>
OpSysPersonal use - categorical list ✅ user inputs check omitted <br>
OpSysProfessional use - categorical list ✅ user inputs check omitted <br>
OfficeStackAsyncHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
OfficeStackAsyncWantToWorkWith - categorical list ✅ user inputs check omitted <br>
OfficeStackSyncHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
OfficeStackSyncWantToWorkWith - categorical list ✅ user inputs check omitted <br>
AISearchHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
AISearchWantToWorkWith - categorical list ✅ user inputs check omitted <br>
AIDevHaveWorkedWith - categorical list ✅ user inputs check omitted <br>
AIDevWantToWorkWith - categorical list ✅ user inputs check omitted <br>
NEWSOSites - categorical list ✅ user inputs check omitted<br>
SOVisitFreq - categorical ✅ checked <br>
SOAccount - categorical ✅ checked <br>
SOPartFreq - categorical ✅ checked <br>
SOComm - categorical ✅ checked <br>
SOAI ✅ Column contains various users opinions about ai, can be great information source for semantic analysis, but for now will be omitted<br>
AISelect - categorical ✅ checked<br>
AISent - categorical ✅ checked<br>
AIAcc - categorical list ✅ user inputs check omitted <br>
AIBen - categorical ✅ checked<br>
AIToolInterested in Using - categorical list ✅ user inputs check omitted <br>
AIToolCurrently Using - categorical list ✅ user inputs check omitted <br>
AIToolNot interested in Using - categorical list ✅ user inputs check omitted <br>
AINextVery different - categorical list ✅ user inputs check omitted <br>
AINextNeither different nor similar - categorical list ✅ user inputs check omitted <br>
AINextSomewhat similar - categorical list ✅ user inputs check omitted <br>
AINextVery similar - categorical list ✅ user inputs check omitted <br>
AINextSomewhat different - categorical list ✅ user inputs check omitted <br>
TBranch - categorical ✅ checked <br>
ICorPM - categorical ✅ checked<br>
WorkExp - integer ❌ <br>
Knowledge_1 - categorical ✅ checked<br>
Knowledge_2 - categorical ✅ checked<br>
Knowledge_3 - categorical ✅ checked<br>
Knowledge_4 - categorical ✅ checked<br>
Knowledge_5 - categorical ✅ checked<br>
Knowledge_6 - categorical ✅ checked<br>
Knowledge_7 - categorical ✅ checked<br>
Knowledge_8 - categorical ✅ checked<br>
Frequency_1 - categorical ✅ checked<br>
Frequency_2 - categorical ✅ checked<br>
Frequency_3 - categorical ✅ checked<br>
TimeSearching - categorical ✅ checked <br>
TimeAnswering - categorical ✅ checked <br>
ProfessionalTech - categorical list ✅ user inputs check omitted <br>
Industry - categorical ✅ checked <br>
SurveyLength ✅ removed <br>
SurveyEase ✅ removed <br>
ConvertedCompYearly - numeric ❌ <br>