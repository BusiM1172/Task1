# Exploratory Data Analysis on the Electoral candidates for the 2021 Municipal elections-South Africa Data Set

## Introduction
This project analyses the Municipal Election candidates for the year 2021. We seek to investigate how far South Africa has come in terms of the levels of representation between genders and age groups in politics. The data set consists of 95 427 records of candidates' names, surnames, ages, political party, province, municipality and ward

## Data Analysis

The data in this task was analysed on jupyter notebook using ;
- pandas
- numpy
- matplotlib
- seaborn

The data was read into a dataframe

### Data Cleaning
We first ensured that the data was prepared for statistical analysis. Data types were determined and were found to be as required. There were also no blank spaces nor NaN values in the data set. However, columns containing candidates' names and surnames were combined to explicitly differentiate between candidates whi similar names or surnames.

### Assessing the Gender numbers in Electoral Candidates
- Plotting a bar chart to see the gender difference in the election candidancy
  sns.histplot(x= 'Gender', data = df)
- Determining the difference in candidancy between males and females in the different provinces
  sns.histplot(x= 'Province', data = df, hue='Gender',multiple = 'dodge')
