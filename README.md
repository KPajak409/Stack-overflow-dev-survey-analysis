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

## Columns checked/processed/removed
ResponseId ✅ unique values
Q120 ✅ removed
MainBranch ❌
Age ❌
Employment ❌
RemoteWork ❌
CodingActivities ✅ checked input answers 
EdLevel ❌ 
LearnCode ✅ checked input answers
LearnCodeOnline ✅ checked input answers
LearnCodeCoursesCert ✅ checked input answers
YearsCode ❌
YearsCodePro ❌
DevType ✅ checked input answers
OrgSize ❌
PurchaseInfluence ❌
TechList ✅ checked input answers
BuyNewTool ✅ checked input answers
Country ❌
Currency ❌
CompTotal ❌
LanguageHaveWorkedWith ✅ checked input answers
LanguageWantToWorkWith ❌
DatabaseHaveWorkedWith ❌
DatabaseWantToWorkWith ❌
PlatformHaveWorkedWith ❌
PlatformWantToWorkWith ❌
WebframeHaveWorkedWith ❌
WebframeWantToWorkWith ❌
MiscTechHaveWorkedWith ❌
MiscTechWantToWorkWith ❌
ToolsTechHaveWorkedWith ❌
ToolsTechWantToWorkWith ❌
NEWCollabToolsHaveWorkedWith ❌
NEWCollabToolsWantToWorkWith ❌
OpSysPersonal use ❌
OpSysProfessional use ❌
OfficeStackAsyncHaveWorkedWith ❌
OfficeStackAsyncWantToWorkWith ❌
OfficeStackSyncHaveWorkedWith ❌
OfficeStackSyncWantToWorkWith ❌
AISearchHaveWorkedWith ❌
AISearchWantToWorkWith ❌
AIDevHaveWorkedWith ❌
AIDevWantToWorkWith ❌
NEWSOSites ❌
SOVisitFreq ❌
SOAccount ❌
SOPartFreq ❌
SOComm ❌
SOAI ❌
AISelect ❌
AISent ❌
AIAcc ❌
AIBen ❌
AIToolInterested in Using ❌
AIToolCurrently Using ❌
AIToolNot interested in Using ❌
AINextVery different ❌
AINextNeither different nor similar ❌
AINextSomewhat similar ❌
AINextVery similar ❌
AINextSomewhat different ❌
TBranch ❌
ICorPM ❌
WorkExp ❌
Knowledge_1 ❌
Knowledge_2 ❌
Knowledge_3 ❌
Knowledge_4 ❌
Knowledge_5 ❌
Knowledge_6 ❌
Knowledge_7 ❌
Knowledge_8 ❌
Frequency_1 ❌
Frequency_2 ❌
Frequency_3 ❌
TimeSearching ❌
TimeAnswering ❌
ProfessionalTech ❌
Industry ❌
SurveyLength ✅ removed
SurveyEase ✅ removed
ConvertedCompYearly ❌


# Conclusions
- User inputs in most questions were trimmed by Stack overflow