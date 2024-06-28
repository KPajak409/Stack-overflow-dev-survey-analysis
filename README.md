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

