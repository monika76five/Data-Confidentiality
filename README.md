# MATH 301-56 Data Confidentiality

Statistical agencies are under legal obligation to protect survey respondents’ privacy when releasing respondent-level data to the public. Statistical models could facilitate such release by introducing perturbation to the original, confidential data. How to develop suitable statistical models, and how to evaluate the privacy protection they produce, are the focus of this Intensive.

## Introduction, Tuesday 1/28/2020

### To-dos

1. Download the ```ACSdata.csv``` file in the datasets folder. Read the data dictionary file to explore this dataset.

2. Scenario \#1: ```SEX = 1, RACE = 1, MAR = 1```

    1. If you know someone with ```SEX = 1, RACE = 1, MAR = 1``` and this person is in this sample, can you find out which record in the sample belongs to this person? What additional information can you learn about this person?
    
    2. If you know someone with ```SEX = 1, RACE = 1, MAR = 1``` but you are not sure if this person is in this sample, what would you do to find this person? What additional information can you learn about this person?
    
3. Scenario \#2: ```SEX = 1, RACE = 1, MAR = 1``` and ```DIS = 1```

    1. If you know someone with ```SEX = 1, RACE = 1, MAR = 1, DIS = 1``` and this person is in this sample, can you find out which record in the sample belongs to this person? What additional information can you learn about this person?
    
    2. Which scenario is more favorable to an intruder, Scenario \#1 vs Scenario \#2?
    
**Make sure to use an R script / R Markdown file to document your work and bring to class.**

