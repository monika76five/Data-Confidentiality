# MATH 301-56 Data Confidentiality

Statistical agencies are under legal obligation to protect survey respondents’ privacy when releasing respondent-level data to the public. Statistical models could facilitate such release by introducing perturbation to the original, confidential data. How to develop suitable statistical models, and how to evaluate the privacy protection they produce, are the focus of this Intensive.

Here is [a growing YouTube playlist of the lecture recordings from Spring 2020](https://www.youtube.com/playlist?list=PL_lWxa4iVNt0XPY0E0MDuGhKvbq_767mr).

## Introduction, Tuesday 1/28/2020

### To-dos (done before class on 1/28)

1. Download the ```ACSdata.csv``` file in the datasets folder. Read the data dictionary file to explore this dataset.

2. Scenario \#1: ```SEX = 1, RACE = 1, MAR = 1```

    1. If you know someone with ```SEX = 1, RACE = 1, MAR = 1``` and this person is in this sample, can you find out which record in the sample belongs to this person? What additional information can you learn about this person?
    
    2. If you know someone with ```SEX = 1, RACE = 1, MAR = 1``` but you are not sure if this person is in this sample, what would you do to find this person? What additional information can you learn about this person?
    
3. Scenario \#2: ```SEX = 1, RACE = 1, MAR = 1``` and ```DIS = 1```

    1. If you know someone with ```SEX = 1, RACE = 1, MAR = 1, DIS = 1``` and this person is in this sample, can you find out which record in the sample belongs to this person? What additional information can you learn about this person?
    
    2. Which scenario is more favorable to an intruder, Scenario \#1 vs Scenario \#2?
    
**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**


## Introduction, Tuesday 2/4/2020

### To-dos (done before class on 2/4)

1. Check out the ```CEsample.csv``` file in the datasets folder. Read the data dictionary file to explore this dataset. Recall that we used this dataset for the topic of Bayesian linear regression in MATH 347.

2. Among the four variables, can you come up with an order of most sensitive to least sensitive? Explain your decision making process.

3. If you decide to use Bayesian synthesis models to generate synthetic values for ```Income```, what models would you use, and why? Please write out the model explicitly.

4. If you decide to use Bayesian synthesis models to generate synthetic values for ```Expenditure```, what models would you use, and why? Please write out the model explicitly.

5. If you decide to use Bayesian synthesis models to generate synthetic values for ```Rural```, what models would you use, and why? Please write out the model explicitly.

6. If you decide to use Bayesian synthesis models to generate synthetic values for ```Race```, what models would you use, and why? Please write out the model explicitly.

7. What if you think both ```Income``` and ```Rural``` are sensitive and you decide to generate synthetic values for them, what kind of approaches can you come up with? If you can, write out the model explicitly.
