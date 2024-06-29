# Stack Overflow Developer survey analysis
Project aims to visualize and analyze data from survey taken by Stack Overflow. It contains wide coveraged information about developers in Information Technology industry.
The easiest and fastest way to see the results is through downloading report in it's pdf, static version i.e there is no interaction between Power BI elements. It can be found in the link below.
\
https://drive.google.com/drive/folders/1p98RDD5DDXIZki91wlc8A2342jdv7c3c?usp=sharing

# Data source
Data utilized in this project comes from widely accesible source i.e [Stack Overflow site](https://insights.stackoverflow.com/survey/). It is annual developer survey performed by Stack Overflow, which is the best known Q&A platform that millions of people visit every month to ask questions, learn, and share technical knowledge. The questions asked each year are selected accordingly to raising trends in Information Technology area and due to it's dynamically changing nature they may differ significantly every year.
## Objectives
This project is going to analyze data from survey taken in 2023. Stack Overflow has already done [analysis](https://survey.stackoverflow.co/2023/) on this survey, but there lays more valuable informations inside this data, which can be obtained with help of visualization.
\
Questions that i would like to answer through analysis of this data:
- In which countries people earn the most?
- How does employment type, education level, organization size and working mode affect the level of pay?
- Which roles are top earners in Poland and knowledge of which programming languages are most valued?
- Does people age affect their trust and likeliness of using AI?
- Is people in any country very unfavorable of AI tools for development?
- Does people who use AI earning more?
- Are you more likely to get a job as a developer if you have a master's degree?

Because of where I live, it will be extremely interesting to analyze only my region and the possibility to compare it with the rest of the world. This would help to draw conclusions about actual situation at the local job market and position it's situation among the rest.

## Structure
Data is placed in two files in csv format. 
- Schema contains information about questions itself, like: question name, content, is it forced to answer, type.
- Public contains information about user answers. Each row corrensponds to single person given answers and each column corrensponds to answer to specific question. In this data there is most of possible types of values stored in columns, like: categorical, numeric, categorical list, intervals.

## Cleaning steps
Stack Overflow stands that dataset is complete and cleaned. By delving into data myself, I was able to find some minor possibilities, to improve the overall quality by applying some of the cleaning steps. Additional steps was also sometimes necessary to visualize data correctly by Power BI. The detailed documentation can be found under descriptive name.


