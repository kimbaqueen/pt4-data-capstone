# Project Overview Description:

- Purpose & what project is, primary features description, challenges/interesting notes about project.

Questions:

- How does gender compare in workplace promotions?
- Does pay gap disparity occur in higher education and higher experienced roles?
- Where are we seeing the biggest gaps between gender compensation?

# Project Tech Stack:

- Jupyter Lab
- SQL
- Python
    > Including: Seaborn, Pandas, Numpy, Matplot lib, Plotly Express libraries
- HTML/CSS

# Dataset Descriptions

## train.csv: https://www.kaggle.com/datasets/shivan118/hranalysis?select=train.csv

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


## Glassdoor Gender Pay Gap.csv: https://www.kaggle.com/datasets/nilimajauhari/glassdoor-analyze-gender-pay-gap

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

- statistics
- visualization of major variables
- checks for missing data
- displays of correlation

# Data Wrangling

- Feature engineering
- data cleansing
- organization of data for modeling

# Statistical Analysis

- linear regression
- output/ interpretation of coefficients
- analysis of p-value, r-squared/other success metrics


# Project Findings / Conclusion
- display of results, insights, conclusions from full project
- display of potential shortfalls of models/insights, and discussion of potential next steps