# Project Overview Description:

*** Refinement needed ***

- Purpose & what project is, primary features description, challenges/interesting notes about project.

Questions:

- How does gender compare in workplace promotions?
- Does pay gap disparity occur in higher education and higher experienced roles?
- Where are we seeing the biggest gaps between gender compensation?

## Project Tech Stack:

- Jupyter Lab
- SQL
- Python
    > Including: Pandas, Numpy, Seaborn, Matplotlib, Plotly Express libraries
- HTML/CSS

# Dataset Descriptions

## train.csv source: https://www.kaggle.com/datasets/shivan118/hranalysis?select=train.csv

### Description: 
HR dataset on employee promotion data with approximately 54,000 rows. Features include education, department, gender, and other columns as described in the data dictionary below. 

| Column | Datatype | Description |
| ------------- |:-------------:| :-----------|
| employee_id | int64 | Employee identification number |
| department | object | Company department employee works in |
| region | object | Company region employee is affiliated with |
| education | object | Level of education completed |
| gender | object | Gender Male / Female |
| recruitment_channel | object | Method employee was recruited |
| no_of_trainings | int64 | Number of trainings completed by employee |
| age | int64 | Employee age (years) |
| previous_year_rating | float64 | Employee’s prior year performance rating |
| length_of_service | int64 | Employee’s length in years at company |
| awards_won? | int64 | Awards won by employee |
| avg_training_score| int64 | Employee average training score |
| is_promoted | int64 | Employee promoted 0 - No, 1 - Yes |


## Glassdoor Gender Pay Gap.csv source: https://www.kaggle.com/datasets/nilimajauhari/glassdoor-analyze-gender-pay-gap

### Description: 
Dataset originated from Glassdoor focusing on job roles and pay, based on gender with approximately 1,000 rows. Features include Job Title, Gender, Age, Base Pay, Bonus, and other columns as described in the data dictionary below. 

| Column | Datatype | Description |
| ------------- |:-------------:| :-----------|
| JobTitle | object | Employee job title|
| Gender | object | Employee gender Male / Female |
| Age | int64 | Employee age (years) |
| PerfEval | int64 | Performance evaluation ranking |
| Education | object | Level of education completed |
| Dept | object | Department employee works in |
| Seniority | int64 | Employee seniority ranking |
| BasePay | int64 | Employee annual base compensation |
| Bonus | int64 | Employee annual bonus |

# Exploratory Data Analysis

## EDA Research 
Each Jupyter notebook includes a review of:
- Basic Statistics
- Visualizations of Major Variables
- Checks for Missing Data
- Research of Correlations
- Reasearch of Pair plots and Relationships

For all Jupyter notebooks, I started exploring each dataset by analyzing what the possible columns are and confirmed data types and data sizes. From there I created subsets using relevant columns data as new variables "train_data_subset", "paygap_data_subset", & "dist_data_subset", respectfully. I researched each dataset for missing values and explored what those missing values data points characteristics look like. I further inspected categorical values to ensure they were standardized and inspected numerical values and how those were distributed with a histogram analysis. No suspicious values found within both the train.csv and Glassdoor Gender Pay Gap.csv datasets. Both were evenly distributed as confirmed via data analysis.

Other notable findings: 
For the distributions_data_2016.csv dataset, after conducting similar analysis as described above, I was able to conclude this dataset size was limited in value counts. It also lacked enough unique values and was not evenly distributed. It also did not have any numerical values that could add value to my project. After this careful consideration, I decided to exclude this dataset from my final project analysis. 


# Data Wrangling

## Tasks Completed
Each Jupyter notebook includes a review of:
- Feature Engineering
- Data Cleansing
- Organization of Data for Modeling

I approached feature engineering by spending quality efforts in exploring the datasets and by creating subsets within each dataframe. This allowed me to choose only relevant features/columns. I also spent time analyzing for null values and where those null values may be trending in the dataset. Categorical values were also confirmed to be standardized. 

This helped with my efficiency when I was to this stage to cleanse the data. I was already familiar with the null values and counts. I was able to anaylze it further from here to determine on the NaN values, how to best replace each column's values. For the education column, it made the most sense to use a "Not Provided" value based on the other categorical responses. For the previous year's rating (performance), I decided to replace values missing to a matching datatype and by using the most common value of 3.0 for this feature in the dataframe. 

In review of the Gender pay gap dataset, while there was no null values to address, I did discover there to be some outliers outside of the 25% & 75% quartiles. After further analysis, I found there was only 9 index rows affected and decided to drop these rows as they were not significant to the overall data population size. 

# Statistical Analysis

## Tasks Completed
Each Jupyter notebook includes a review of:
- linear regression
- output/ interpretation of coefficients
- analysis of p-value, r-squared/other success metrics

Using Seaborn & matplotlib, I approached by analysing pairplots to find relationships worth exploring more in depth. I was able to find features that did have relationships such as Age & BasePay, and Bonus & BasePay. I further researched the relationships by running regression plots and inspecting the outputs by using KDE, pairplots, heatmaps to discover coefficient trends. 

I found using regplot was excellent to showcase the negative/positive trends and ability to stylize it for demonstrations would be very useful in real world applications. For p-value, scipy stats was imported to analyze. Unfortunately the annotate function to add was deprecated. This will be added onto future feature versions of this project.

# Project Findings / Conclusion

*** Refinement needed ***

- display of results, insights, conclusions from full project
- display of potential shortfalls of models/insights, and discussion of potential next steps
- talk about many contributing factors, equal pay days change every year for women & minorities & links to other helpful info
