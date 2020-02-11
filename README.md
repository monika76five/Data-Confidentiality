# MATH 301-56 Data Confidentiality

Statistical agencies are under legal obligation to protect survey respondents’ privacy when releasing respondent-level data to the public. Statistical models could facilitate such release by introducing perturbation to the original, confidential data. How to develop suitable statistical models, and how to evaluate the privacy protection they produce, are the focus of this Intensive.

Here is [the tentative schedule](https://docs.google.com/spreadsheets/d/119NV9ZkKvPD0r-5N3AlDxbNZUpVK1Lr7j2WX7xL1FHU/edit?usp=sharing).

Here is [a growing YouTube playlist of the lecture recordings from Spring 2020](https://www.youtube.com/playlist?list=PL_lWxa4iVNt0XPY0E0MDuGhKvbq_767mr).

Office hours: Wednesdays 10am-12pm and Thursdays 11:30am-12:30pm @ RH 403.

## Introduction, Tuesday 1/28/2020

### To-do (done before class on 1/28)

1. Download the ```ACSdata.csv``` file in the datasets folder. Read the data dictionary file to explore this dataset.

2. Scenario \#1: ```SEX = 1, RACE = 1, MAR = 1```

    1. If you know someone with ```SEX = 1, RACE = 1, MAR = 1``` and this person is in this sample, can you find out which record in the sample belongs to this person? What additional information can you learn about this person?
    
    2. If you know someone with ```SEX = 1, RACE = 1, MAR = 1``` but you are not sure if this person is in this sample, what would you do to find this person? What additional information can you learn about this person?
    
3. Scenario \#2: ```SEX = 1, RACE = 1, MAR = 1``` and ```DIS = 1```

    1. If you know someone with ```SEX = 1, RACE = 1, MAR = 1, DIS = 1``` and this person is in this sample, can you find out which record in the sample belongs to this person? What additional information can you learn about this person?
    
    2. Which scenario is more favorable to an intruder, Scenario \#1 vs Scenario \#2?
    
**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**


## Bayesian Synthesis Models \# 1, Tuesday 2/4/2020

### To-do (done before class on 2/4)

1. Check out the ```CEdata.csv``` file in the datasets folder. Read the data dictionary file to explore this dataset. Recall that we used this dataset for the topic of Bayesian linear regression in MATH 347.

2. Among the four variables, can you come up with an order of most sensitive to least sensitive? Explain your decision making process.

3. If you decide to use Bayesian synthesis models to generate synthetic values for ```Income```, what models would you use, and why? Please write out the model explicitly.

4. If you decide to use Bayesian synthesis models to generate synthetic values for ```Expenditure```, what models would you use, and why? Please write out the model explicitly.

5. If you decide to use Bayesian synthesis models to generate synthetic values for ```UrbanRural```, what models would you use, and why? Please write out the model explicitly.

6. If you decide to use Bayesian synthesis models to generate synthetic values for ```Race```, what models would you use, and why? Please write out the model explicitly.

7. What if you think both ```Income``` and ```UrbanRural``` are sensitive and you decide to generate synthetic values for both of them, what kind of approaches can you come up with? If you can, write out the model explicitly.

**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**


## Bayesian Synthesis Models \# 2, Tuesday 2/11/2020

### To-do (done before class on 2/11)

1. Check out the lecture slides (S20MATH301_BayesianSynthesisModels.pdf), especially pages 23-29, and digest how to generate ```m = 1``` synthetic dataset and how to generate ```m = 20``` synthetic datasets. Specifically, pay attention to how we are using the posterior draws of ```beta_0, beta_1, sigma```.

2. Use your own synthesis model (different from the simple linear regression we covered in class) to synthesize ```m = 1``` synthetic dataset for the CE sample. 
    1. Make a scatter plot of the synthesized ```log(Income)``` against the original ```log(Income)```, and see what you find.
    2. Compare the mean and median of ```log(Income)```, in the original dataset and the confidential dataset. Are they close to each other?
    3. Compare the point estimate of the regression coefficients of ```log(Income)``` on ```log(Expenditure)```, in the original dataset and the confidential dataset. Are they close to each other? 
    
3. Read ```Kinney et al (2011)``` in the References folder, and prepare answers to the following questions.
    1. What are the synthesized and un-synthesized variables in the SynLBD?
    2. What approaches did they take when they have more than 1 variables deemed sensitive and to be synthesized?
    3. What Bayesian synthesis model(s) did they use? Details of the synthesis models are in ```Kinney et al (2011) appendix```.
    4. How many synthetic datasets did they generate?
    5. How did they evaluate the utility of the synthetic datasets? Can you think of any other utility measures?
    6. How did they evaluate the disclosure risks? Can you think of any other disclosure risks measures?
    
4. Start thinking about your course project! What public use datasets that you think are risky? It might be a good idea to find appropriate datasets as soon as you can.

**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**


## Methods for Utility Evaluation, Tuesday 2/18/2020

### To-do (done before class on 2/18)

1. Read ```Kinney et al (2011)``` in the References folder, and prepare answers to the following questions.
    1. What are the synthesized and un-synthesized variables in the SynLBD?
    2. What approaches did they take when they have more than 1 variables deemed sensitive and to be synthesized?
    3. What Bayesian synthesis model(s) did they use? Details of the synthesis models are in ```Kinney et al (2011) appendix```.
    4. How many synthetic datasets did they generate?
    5. How did they evaluate the utility of the synthetic datasets? Can you think of any other utility measures?
    6. How did they evaluate the disclosure risks? Can you think of any other disclosure risks measures?
    
2. Read ```Woo et al (2009)``` in the References folder, and prepare answers to the following questions.
    1. What are the pros and cons of analysis-specific measures?
    2. What are the pros and cons of global measures?
    3. What are the similaries between the proposed global measures?
    4. <ins>Evaluate the global utility measures of your synthesized ```log(Income)``` from your Bayesian synthesis model for the CE sample.</ins>
    5. Which global measure do you think works the best? The least? Give explanations.
    
3. <ins>Find one or more datasets and demonstrate potential disclosure risks. You can start with identification disclosure.</ins>

**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**
