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
CompTotal ❌ <br>
LanguageHaveWorkedWith ✅ checked input answers <br>
LanguageWantToWorkWith ❌ <br>
DatabaseHaveWorkedWith ❌ <br>
DatabaseWantToWorkWith ❌ <br>
PlatformHaveWorkedWith ❌ <br>
PlatformWantToWorkWith ❌ <br>
WebframeHaveWorkedWith ❌ <br>
WebframeWantToWorkWith ❌ <br>
MiscTechHaveWorkedWith ❌ <br>
MiscTechWantToWorkWith ❌ <br>
ToolsTechHaveWorkedWith ❌ <br>
ToolsTechWantToWorkWith ❌ <br>
NEWCollabToolsHaveWorkedWith ❌ <br>
NEWCollabToolsWantToWorkWith ❌ <br>
OpSysPersonal use ❌ <br>
OpSysProfessional use ❌ <br>
OfficeStackAsyncHaveWorkedWith ❌ <br>
OfficeStackAsyncWantToWorkWith ❌ <br>
OfficeStackSyncHaveWorkedWith ❌ <br>
OfficeStackSyncWantToWorkWith ❌ <br>
AISearchHaveWorkedWith ❌ <br>
AISearchWantToWorkWith ❌ <br>
AIDevHaveWorkedWith ❌ <br>
AIDevWantToWorkWith ❌ <br>
NEWSOSites ❌ <br>
SOVisitFreq ❌ <br>
SOAccount ❌ <br>
SOPartFreq ❌ <br>
SOComm ❌ <br>
SOAI ❌ <br>
AISelect ❌ <br>
AISent ❌ <br>
AIAcc ❌ <br>
AIBen ❌ <br>
AIToolInterested in Using ❌ <br>
AIToolCurrently Using ❌ <br>
AIToolNot interested in Using ❌ <br>
AINextVery different ❌ <br>
AINextNeither different nor similar ❌ <br>
AINextSomewhat similar ❌ <br>
AINextVery similar ❌ <br>
AINextSomewhat different ❌ <br>
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