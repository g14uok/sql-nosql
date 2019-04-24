# SQL/NoSQL
# Final Project
## Jeevan Rachepalli and Kathleen DeBrota
## Spring 2019

# From the final project assignment page (delete later):

Engineering Project: Building up a database to demonstrate interesting searches

1-3 students form one group
Select one interesting domain or problem, building your database using any database systems (SQL and/or NoSQL)
Demonstrating or visualizing various queries and query results
Setting up a running website which is able to display/visualize query and query results (optional, for those who aim for a high score)
Expected Result:

You should submit: (1) a project report (state clearly the contribution from each team member if you work with others. It should be 4-8 pages); (2) a demo video (just like you present your project to classmates... you can share your slide in the video when you present); (3) the slide used in your video; and (4) other material (e.g., codes, visualizations, SQL dumps, etc.) if applicable.
***
# Division of tasks:
Both: Structuring SQL database, writing report, recording video, writing SQL queries, data cleaning as needed, attend meetings
Jeevan: Find data, preprocessing, cleaning, Python visualizations (if needed), setup GitHub page
Kathleen: Structuring research questions, visualizations (R), statistics based on queries (R), setup Google doc and google presentation
***
# For the final report, these sections should be included:

## Data description:
- size, shape, content, datatypes of data; meaning of each column, what the values represent
- source of data (kaggle link), why it is useful/why it was collected and when, etc

## Pre-Processing the data
- Dataset does not contain any missing values.

- Converted gender values in "SEX" column from:
      1 -> male
      2 -> female
- Converted the values in "MARRIAGE" column from:
      0 -> unknown
      1 -> married
      2 -> single
      3 -> others
- Converted the values in "EDUCATION" column from:
      0 -> uneducated
      1 -> graduate
      2 -> under graduate
      3 -> high school
      4 -> others
      5 -> unknown
      6 -> unknown

- Renamed the column "PAY_0" to "PAY_1" 
- Renamed the column "default.payment.next.month" to "DEFAULT_PAYMENT_NEXT_MONTH" 

## Guiding research questions and queries to write to answer them:
- Overarching question is, "Who (what kind of person) is most likely to delay payment on their credit card bill and/or default their payments?"
- Are younger people more or less likely to default on their payments?
      -- Sort query by age ascending AND 'likelihood of defaulting'==1
      -- Can also discretize this if we want...put ages into bins, then run stats on the different bins?

- Are higher-educated people more or less likely to default on their payments?
      -- sort query by education ascending and 'likelihood of defaulting'==1
      -- Can run stats on the distributions falling into each education category

- How is credit limit associated with likelihood to default? How is credit limit associated with age and education level?
      -- Maybe make use of 'bins' and put people with different credit limits into bins to discretize. Then sort by (will default next month AND credit limit(desc))
      -- linear regression of these two variables, check the stats on the regression

- At what bill value is someone more likely to default on their payment? Are there any demographic trends that emerge there?
      -- Get (demographic values) filtered by (deferred payment by 9 months or more (or the 'will default next month' variable)) sort by (bill value descending)
      -- visualization for this could be a paired bar chart maybe? Probably a better option in R/Python/Tableau

- MORE QUERIES?
