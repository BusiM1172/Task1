# Exploratory Data Analysis on the Electoral candidates for the 2021 Municipal elections-South Africa Data Set
## TABLE OF CONTENTS
1. INTRODUCTION
2. DATA ANALYSIS
     2.1 Data Preparation
     2.2 Assessing the Gender numbers in Electoral Candidates
          2.2.1 Findings
     2.3 Assessing the Age representation in the Electroral Candidates
          2.3.1 Findings
     
## 1. Introduction
This project analyses the Municipal Election candidates for the year 2021. We seek to investigate how far South Africa has come in terms of the levels of representation between genders and age groups in politics. The data set consists of 95 427 records of candidates' names, surnames, ages, political party, province, municipality and ward

## 2. Data Analysis

The data in this task was analysed on jupyter notebook using ;
- pandas
- numpy
- matplotlib
- seaborn

The [data](voting_candidate.csv) was read into a [dataframe](voting_candidates.ipynb)
* df= pd.read_csv('voting_candidate.csv')

### 2.1 Data Preparation
We first ensured that the data was prepared for statistical analysis. Data types were determined and were found to be as required. There were also no blank spaces nor NaN values in the data set. However, columns containing candidates' names and surnames were combined to explicitly differentiate between candidates with similar names or surnames.

### 2.2 Assessing the Gender numbers in Electoral Candidates
- The number of unique individuals (taking care of the fact that some may have stood for more than one position) who stood for the elections
    * df.nunique()
- The male and female count was determined for the ENTIRE election
    * sns.histplot(x= 'Gender', data = df)
- The male and female count was also determined for the different provinces
 - It was found that there was a higher male candidate count in the political parties. A few exceptions exist in some small parties, namely;
    * Agency for New Change
    * Allied Movement for Change
    * Batho Pele Movement

### 2.3 Assessing the Age representation in the Electroral Candidates
- The distribution of the ages of all the candidates was determined
    * grouped_age= df.groupby(['Age']).count()
    * grouped_age.plot(x='Age', y='Name', figsize=(10, 8), kind='scatter')
- The distribution of age in the different political parties was determined
    * sns.barplot(x ='Party/Indep', y ='Name', data= grouped_party1, hue ='Gender')

    ### 2.3.1 Findings
    * The youngest candidate is 18 years old and the oldest 93 year old. 
    * The average age of the candidates is 44 years. 
    * The age distribution of this candidate list can be viewed as a healthy one that would ensure continuity. 
A report with all the visualisations and conclusions was compiled
