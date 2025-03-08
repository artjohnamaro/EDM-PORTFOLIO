# Midterm Lab Task 2- – Data Cleaning and Transformation Using Power Query Editor

## Task Description:
Company X would like to extract some useful information from the UnclenedDSJObs csv taken
from a Job Posting site available in Kaggle. There are a lot of columns available but focus only
on generating insights that will answer the ff: questions
1. exWhich Job Roles pay the highest and least
2. What size companies pay the best
3. Where Job Roles or Job Titles pay the best and least in a specific state

## Instructions:

**1. Download the copy of the dataset (Uncleaned_DS_jobs.csv)**

**2. Load the Data in Excel – Open Excel – Goto Data – New Query Open File – text/csv**

**3. Load – Edit the Dataset using Power Query Editor**

**4. Duplicate the raw data**

**5. Here are your data-cleaning task:**

**a. Salary Estimate Column – Remove All the characters after the ( open
parentheses) by GOING to**

i. Transform Menu -> Extract

ii. Select Text Before Delimiter

iii. Type (

iv. Click Ok to apply Extract task

**b. Create 2 New Columns (From the Salary Estimate) Min Sal and Max Sal**

i. To Create a Min Sal – Select Salary Estimate Column

ii. Goto Add Column Menu

iii. Select Column from Examples

iv. Select From Selections

**c. ADD COLUMN – Role Type**
i. Goto Add Column Menu

ii. Click Custom Column

iii. Change Column Name to Role Type

iv. Then type this formula:

if Text.Contains([Job Title], "Data Scientist") then
"Data Scientist"

else if Text.Contains([Job Title], "Data Analyst") then
"Data Analyst"

else if Text.Contains([Job Title], "Data Engineer") then
"Data Engineer"

else if Text.Contains([Job Title], "Machine Learning") then
"Machine Learning Engineer"

else
"other"
- Change Data Type to Text (Right click the column head then change Type to
text

**Note: This will group the Job Titles into 5 groups only**

**d. SPLIT COLUMNS by Delimeter**
**e. Select Location column (SPLIT columns by , Delimeter)**
**i. Problem is not all entries have , delimeters i.e New Jersey, United States
etc...**
**ii. Hence you need to perform some Custom Columns First
with the ff: formula**

if [Location]= "New Jersey" then ", NJ"

else if [Location] = "Remote" then ", other"

else if [Location]= "United States" then ", other"

else if [Location]= "Texas" then ", TX"

else if [Location]= "Patuxent" then ", MA"

else if [Location]= "California" then ", CA"

else if [Location]= "Utah" then ", UT"

else [Location]


iii. Click ok then Location Correction Column will be created
iv. Select Location Correction Column
1. Select the new Custom Column
2. Goto Transform
3. Click Split Column BY Delimeter
4. Choose , comma
5. Then ok to Apply the split
6. A Location Correction 1 and Location Correction Column 2 will be
created

v. Filter New Column(Select Location Correction 2) –
to check outliers (Anne Rundell)
1. Under Transform Menu – Replace Values Find Anne Rundell and
replaced with “MA”
2. Rename Column(Location Correction 2) with State Abbreviations

vi. Split the size Column and create 2 new column

1. Create a new Column for the MinCompanySize and
MaxCompanySize

3. (Follow the same splitting column method as you did in Salary
Estimate)

vii. Handle negative values

1. (See competitors column) filter all -1’s
2. See revenues column filter 0’s
3. See industry column filter -1’s
viii. Clean Company name and remove Rates after the name of company
ix. Remove Column Descriptions

f. Copy the APPLIED steps as proof of your Data Cleaning Activities ->

i. Go to Home Menu – Click Advanced Editor. Copy and paste the file in your
portfolio

## Part 2. Reshape and Group the tables:

**1. Create a duplicate of the raw data Right Click Unclean DS Jobs select
duplicate (Queries pane)**

**2. Rename the duplicate with “Sal By Role Type dup”**

 a. Click Choose Columns
 
 b. Select Role Type, Min Sal and Max Sal
 
 c. Change Data Type of min and max sal to currency
 
 d. then multiply Min and Max Lal columns by 1000 (By going to
Numbers Column – Click Standard -> Multiply – Type 100)

e. Then Group the rows by role type and get the min sal and
max sal average

f. Select the role type column - > click Group By under
Transform Menu

g. Then Group the rows by role type and get the average

**3. Create a reference of the raw data Right Click Unclean DS Jobs
choose reference (Queries pane)**

**4. Rename the reference with “Sal By Role Size ref”**

a. Click Choose Columns

b. Select Size, Min Sal and Max Sal

c. Change Data Type of min and max sal to currency then
multiply by 1000

d. Then Group the rows by size and get the min sal and max sal
average

e. Select the size column - > click Group By under Transform
Menu

**5. Mapping Other Files and include in the current queries**
a. Click Unclean DS Jobs

b. Click on any white space in the Queries pane Right Click –

New Query -> Open the Workbook State Mapping – Select

the columns – Click Ok

c. It should be now included in the queries

d. Select Uncleaned DS jobs from the queries

e. Select state abbreviation (on both queries)

f. Select Merge – as shown

g. Click ok

h. It should now match the State Abbreviation with the merge
state

i. Rename Columns as State Full Name

j. Filter state Abbreviations and remove nulls and blanks

**6. Create a reference of the raw data Right Click Unclean DS Jobs
choose reference (Queries pane)**

**7. Rename the reference with “Sal By State ref”**

a. Click Choose Columns

b. Select State Full Name, Min Sal and Max Sal

c. Change Data Type of min and max sal to currency then
multiply by 1000

d. Then Group the rows by State FullName and get the min sal
and max sal average

e. Select the size column - > click Group By under Transform
Menu

**5. Mapping Other Files and include in the current queries**
a. Click Unclean DS Jobs

b. Click on any white space in the Queries pane Right Click –
New Query -> Open the Workbook State Mapping – Select
the columns – Click Ok

c. It should be now included in the queries

d. Select Uncleaned DS jobs from the queries

e. Select state abbreviation (on both queries)

f. Select Merge – as shown

g. Click ok

h. It should now match the State Abbreviation with the merge
state

i. Rename Columns as State Full Name

j. Filter state Abbreviations and remove nulls and blanks

**6. Create a reference of the raw data Right Click Unclean DS Jobs
choose reference (Queries pane)**


