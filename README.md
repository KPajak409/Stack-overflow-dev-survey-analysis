# Data cleaning

## Drop unnecessary columns
- Q120 - empty question in schema filled with one unique value without nulls, possibly consent to processing data.
- SurveyLength, SurveyEase question about the respondent's feelings after completing the survey may be omitted.
- SOAI long strings containing user opinions about AI, great for NLP, not exactly for this project
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

## Columns checked/processed/removed
ResponseId ✅ unique values <br>
Q120 ✅ removed <br>
MainBranch ❌ <br>
Age ❌ <br>
Employment ❌ <br>
RemoteWork ❌ <br>
CodingActivities ✅ checked input answers <br> 
EdLevel ❌ <br> 
LearnCode ✅ checked input answers <br>
LearnCodeOnline ✅ checked input answers <br>
LearnCodeCoursesCert ✅ checked input answers <br>
YearsCode ❌ <br>
YearsCodePro ❌ <br>
DevType ✅ checked input answers <br>
OrgSize ❌ <br>
PurchaseInfluence ❌ <br>
TechList ✅ checked input answers <br>
BuyNewTool ✅ checked input answers <br>
Country ❌ <br>
Currency ❌ <br>
CompTotal ✅ casted to int, removed unreal values <br>
LanguageHaveWorkedWith ✅ checked input answers <br>
LanguageWantToWorkWith ❌ user inputs check omitted <br>
DatabaseHaveWorkedWith ❌ user inputs check omitted <br>
DatabaseWantToWorkWith ❌ user inputs check omitted <br>
PlatformHaveWorkedWith ❌ user inputs check omitted <br>
PlatformWantToWorkWith ❌ user inputs check omitted <br>
WebframeHaveWorkedWith ❌ user inputs check omitted <br>
WebframeWantToWorkWith ❌ user inputs check omitted <br>
MiscTechHaveWorkedWith ❌ user inputs check omitted <br>
MiscTechWantToWorkWith ❌ user inputs check omitted <br>
ToolsTechHaveWorkedWith ❌ user inputs check omitted <br>
ToolsTechWantToWorkWith ❌ user inputs check omitted <br>
NEWCollabToolsHaveWorkedWith ❌ user inputs check omitted <br>
NEWCollabToolsWantToWorkWith ❌ user inputs check omitted <br>
OpSysPersonal use ❌ user inputs check omitted <br>
OpSysProfessional use ❌ user inputs check omitted <br>
OfficeStackAsyncHaveWorkedWith ❌ user inputs check omitted <br>
OfficeStackAsyncWantToWorkWith ❌ user inputs check omitted <br>
OfficeStackSyncHaveWorkedWith ❌ user inputs check omitted <br>
OfficeStackSyncWantToWorkWith ❌ user inputs check omitted <br>
AISearchHaveWorkedWith ❌ user inputs check omitted <br>
AISearchWantToWorkWith ❌ user inputs check omitted <br>
AIDevHaveWorkedWith ❌ user inputs check omitted <br>
AIDevWantToWorkWith ❌ user inputs check omitted <br>
NEWSOSites ❌ <br>
SOVisitFreq ❌ <br>
SOAccount ❌ <br>
SOPartFreq ❌ <br>
SOComm ❌ <br>
SOAI ❌ Column contains various users opinions about ai, can be great information source for semantic analysis, but for now will be omitted<br>
AISelect ❌ <br>
AISent ❌ <br>
AIAcc ❌ user inputs check omitted <br>
AIBen ❌ <br>
AIToolInterested in Using ❌ user inputs check omitted <br>
AIToolCurrently Using ❌ user inputs check omitted <br>
AIToolNot interested in Using ❌ user inputs check omitted <br>
AINextVery different ❌ user inputs check omitted <br>
AINextNeither different nor similar ❌ user inputs check omitted <br>
AINextSomewhat similar ❌ user inputs check omitted <br>
AINextVery similar ❌ user inputs check omitted <br>
AINextSomewhat different ❌ user inputs check omitted <br>
TBranch ❌ <br>
ICorPM ❌ <br>
WorkExp ❌ <br>
Knowledge_1 ❌ <br>
Knowledge_2 ❌ <br>
Knowledge_3 ❌ <br>
Knowledge_4 ❌ <br>
Knowledge_5 ❌ <br>
Knowledge_6 ❌ <br>
Knowledge_7 ❌ <br>
Knowledge_8 ❌ <br>
Frequency_1 ❌ <br>
Frequency_2 ❌ <br>
Frequency_3 ❌ <br>
TimeSearching ❌ <br>
TimeAnswering ❌ <br>
ProfessionalTech ❌ <br>
Industry ❌ <br>
SurveyLength ✅ removed <br>
SurveyEase ✅ removed <br>
ConvertedCompYearly ❌ <br>


# Conclusions
- User inputs in most questions were trimmed by Stack overflow