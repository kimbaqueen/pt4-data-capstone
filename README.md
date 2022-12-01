# Project Overview Description:

This project's purpose is to research gender pay biases, particularly for women in the United States. Using data gathered primarily from Glassdoor, I examined trends of how women across different job titles and functions pay is affected. Primary features included Base Pay, Job Department & Titles, Gender, and Age. 

Some challenges I overcame was finding diversified data on gender pay gap in my initial project exploration phase. It was further difficult to find transparent data for women of color and other underrepresented groups and pay biases. This project is interesting to me because since the onset of the COVID pandemic, there has been more workplace talk of equity and inclusion. U.S. Companies are spending $8 Billion annually, historically more now than ever, on DEI initiatives but yet pay gap disparity continues to be a hot topic[^1]. 

[^1]: https://fortune.com/2021/12/07/metrics-diversity-inclusion-workplace-careers-joan-williams/


## Questions:

- How does compensation compare in the current workplace between genders?
- Do pay gap biases trends exist across different Job functions?
- Where are we seeing the greatest compensation biases?

## Project Tech Stack:

- Jupyter Lab
- SQL
- Python
    > Including: Pandas, Numpy, Seaborn, Matplotlib, Plotly Express, Scipy libraries
- HTML/CSS
    > Bonus Materials: I also utilized methods that were not covered in our DevMountain Data Analytics coursework, including an informational data dashboard & website design, FacetGrid and advanced visualization styling effects. For my project webpage design, I also was careful to include mobile responsive design and styling outside of the foundations and data analytics program's scope. 

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

This helped with my efficiency when I was to this stage to cleanse the data. I was already familiar with the null values and counts. I was able to analyze it further from here to determine on the NaN values, how to best replace each column's values. For the education column, it made the most sense to use a "Not Provided" value based on the other categorical responses. For the previous year's rating (performance), I decided to replace values missing to a matching datatype and by using the most common value of 3.0 for this feature in the dataframe. 

In review of the Gender pay gap dataset, while there was no null values to address, I did discover there to be some outliers outside of the 25% & 75% quartiles. After further analysis, I found there was only 9 index rows affected and decided to drop these rows as they were not significant to the overall data population size. 

# Statistical Analysis

## Tasks Completed
Each Jupyter notebook includes a review of:
- linear regression
- output/ interpretation of coefficients
- analysis of p-value, r-squared/other success metrics

Using Seaborn & matplotlib, I approached by analyzing pairplots to find relationships worth exploring more in depth. I was able to find features that did have relationships such as Age & BasePay, and Bonus & BasePay. I further researched the relationships by running regression plots and inspecting the outputs by using KDE, pairplots, heatmaps to discover coefficient trends. 

I found using regplot was excellent to showcase the negative/positive trends and ability to stylize it for demonstrations would be very useful in real world applications. For p-value, scipy stats was imported to analyze. Unfortunately the annotate function to add was deprecated. This will be added onto future feature versions of this project.

# Project Findings / Conclusion

## Findings

- Women still experience pay equity biases in the workplace today.
- Women are majority at a disadvantage for both pay parity and representation across job titles and functions.
- The largest gender pay bias was found amongst the Engineering department, followed by Administrative & Sales department roles.

After examining the data, it was clear that gender equity pay biases still exist today. While there are many underlying factors at play, our dataframe sets confirmed that women were trending below men on the pay scale across departments and job functions as a majority.

In terms of representation, Women made up more than 90% of the Marketing Associate roles. However, this was one of the highest disparity job title groups for base pay between genders. The Engineering department had the largest difference of average base pay between genders, with women making up less than 10% of this department for comparison.

Other interesting findings were Base Pay and Bonus Pay were negatively correlated for both genders. Age and Base Pay was positively correlated for both genders. Still, when analyzing Average Base Pay against age between genders, women were still trailing behind in all department categories.

Potential shortfalls of this project are around the data collection and integrity of data reported online. There is not much transparency in salaries across job functions, gender, and other HR sensitive metrics. Even if a company does have this information, they may not make it publicly available due to fear of public retaliation or other legal implication risks.

In future enhancements to this project's research, I'd like to find and explore more specific data on women of color and other underrepresented groups. In particular, representation of women of color rising the ranks in leadership roles across departments and industries, and their respective salaries in comparison to caucasian women and men.

## Get Involved

While having conversations in the workplace about DEI is important, it's not enough. To impact meaningful change we must be willing to accept some degree of risk and take a candid inventory of where your company stands. Look for meaningful metrics. Treat DEI like any other company initiative that needs to get results and be ready to act on what you find[^2]. 

[^2]: https://hbr.org/2022/03/data-driven-diversity

- Research. Stay informed. Become actively involved in your community.
- Advocate. Be an Ally.
- Mentor and Sponsor Women & Underrepresented Groups.

### Additional Resources & Recommended Articles on the project webpage

Demo Video: https://youtu.be/4Xb1bGlN4d0
Project Webpage: https://kimbaqueen.github.io/DMDataCapstone/index.html
