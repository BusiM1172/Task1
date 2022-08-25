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

### Data Preparation
We first ensured that the data was prepared for statistical analysis. Data types were determined and were found to be as required. There were also no blank spaces nor NaN values in the data set. However, columns containing candidates' names and surnames were combined to explicitly differentiate between candidates with similar names or surnames.

### Assessing the Gender numbers in Electoral Candidates
- The number of unique individuals (taking care of the fact that some may have stood for more than one position) who stood for the elections
-   df.nunique()
- The male and female count was determined for the ENTIRE election
    sns.histplot(x= 'Gender', data = df)
- The male and female count was also determined for the different provinces
  sns.histplot(x= 'Province', data = df, hue='Gender',multiple = 'dodge')
- The male and female count was also determined for the different political parties
  
  ### Findings
 - There was generally a higher count of males compared to females in all provinces. 
 - The 3 provinces with significantly higher male representation are Gauteng, KwaZulu Natal and the Western Cape. The Northern Cape has the smallest difference between the genders.  The table below shows that 62% of the candidates were male. 
 - It was found that there was a higher male candidate count in the political parties. A few exceptions exist in some small parties, namely;
    * Agency for New Change
    * Allied Movement for Change
    * Batho Pele Movement

### Assessing the Age representation in the Electroral Candidates
