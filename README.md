# MATH 301-56 Data Confidentiality

Statistical agencies are under legal obligation to protect survey respondents’ privacy when releasing respondent-level data to the public. Statistical models could facilitate such release by introducing perturbation to the original, confidential data. How to develop suitable statistical models, and how to evaluate the privacy protection they produce, are the focus of this Intensive.

Here is [the tentative schedule](https://docs.google.com/spreadsheets/d/119NV9ZkKvPD0r-5N3AlDxbNZUpVK1Lr7j2WX7xL1FHU/edit?usp=sharing).

Here is [a growing YouTube playlist of the lecture recordings from Spring 2020](https://www.youtube.com/playlist?list=PL_lWxa4iVNt0XPY0E0MDuGhKvbq_767mr).

Here is our [Zoom meeting link](https://vassar.zoom.us/j/829733465), beginning on Tuesdsay 3/24.

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
    
3. Read ```Kinney et al. (2011)``` in the References folder, and prepare answers to the following questions.
    1. What are the synthesized and un-synthesized variables in the SynLBD?
    2. What approaches did they take when they have more than 1 variables deemed sensitive and to be synthesized?
    3. What Bayesian synthesis model(s) did they use? Details of the synthesis models are in ```Kinney et al. (2011) appendix```.
    4. How many synthetic datasets did they generate?
    5. How did they evaluate the utility of the synthetic datasets? Can you think of any other utility measures?
    6. How did they evaluate the disclosure risks? Can you think of any other disclosure risks measures?
    
4. Start thinking about your course project! What public use datasets that you think are risky? It might be a good idea to find appropriate datasets as soon as you can.

**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**


## Methods for Utility Evaluation \#1, Tuesday 2/18/2020

### To-do (done before class on 2/18)

1. Read ```Kinney et al. (2011)``` in the References folder, and prepare answers to the following questions.
    1. What are the synthesized and un-synthesized variables in the SynLBD?
    2. What approaches did they take when they have more than 1 variables deemed sensitive and to be synthesized?
    3. What Bayesian synthesis model(s) did they use? Details of the synthesis models are in ```Kinney et al (2011) appendix```.
    4. How many synthetic datasets did they generate?
    5. How did they evaluate the utility of the synthetic datasets? Can you think of any other utility measures?
    6. How did they evaluate the disclosure risks? Can you think of any other disclosure risks measures?
    
2. Read ```Woo et al. (2009)``` in the References folder, and prepare answers to the following questions.
    1. What are the pros and cons of analysis-specific measures?
    2. What are the pros and cons of global measures?
    3. What are the similaries between the proposed global measures?
    4. <ins>Evaluate the global utility measures of your synthesized ```log(Income)``` from your Bayesian synthesis model for the CE sample.</ins>
    5. Which global measure do you think works the best? The least? Give explanations.
    
3. <ins>Find one or more datasets and **demonstrate potential disclosure risks in the original data**. You can start with identification disclosure. If you are working with continuous variables, be creative about how you calculate the identification disclosure risks.</ins>

**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**


## Methods for Utility Evaluation \#2, Tuesday 2/25/2020

### To-do (done before class on 2/25)

1. Read ```Woo et al. (2009)``` in the References folder, and prepare answers to the following questions.
    1. What are the pros and cons of analysis-specific measures?
    2. What are the pros and cons of global measures?
    3. What are the similaries between the proposed global measures?
    4. <ins>Evaluate the global utility measures of your synthesized ```log(Income)``` from your Bayesian synthesis model for the CE sample.</ins>
    5. Which global measure do you think works the best? The least? Give explanations.
    
2. <ins>Read ```Drechsler (2001) Chapter 6-1, 7-1``` in the References folder, and prepare the following results.</ins>
    1. <ins>Generate ```m = 20``` synthetic datasets given your synthesis model for the CE sample. If you are using ```set.seed()```, make sure that you do not generate the same synthetic data for each ```m = 20```.</ins>
    2. <ins>Estimate a few analysis-specific utility measures, e.g. the mean and median of a continuous synthetic variable, the regression analysis coefficients, for each synthetic dataset.</ins>
    3. <ins>Use the combining rules in ```Drechsler 2001 Chapter 6-1``` (for fully synthetic data) and / or ```Drechsler 2001 Chapter 7-1``` (for partially synthetic data) and create your final point estimate and confidence interval of the analysis-specific utility measures you calculated in Item ii above.</ins>
    
3. <ins>Read ```Drechsler, J. and Reiter, J. P. (2009)``` in the References folder (focus on Section 2.3 about the interval overlap utility measure), and prepare the following results.</ins>
    1. <ins>Calcuate the corresponding interval overlap measure for each of the analysis-specific utility measures you have done in Item 2.ii above.</ins>

4. <ins>**Present your synthesis model(s) for your project dataset(s)**. Refer to the Bayesian Synthesis Models \#1 and \#2 lectures for different synthesis models we have covered, and possibly the references in Item 5 below for ordered categorical data synthesis and count data synthesis.</ins>

5. Additional synthesis models for other variable types:
    1. Ordered categorical: **probit regression**. Check out ```Hoff, P. (2009)``` (textbook for MATH 347),  **Section 12.1.1**. Note that the book gives sample R script for writing your own MCMC. Dig around to see how to use JAGS for implementation.
    2. Count: **Poisson regression**. Check out ```Hoff, P. (2009)``` (textbook for MATH 347), **Section 10.1**. Note that the book gives sample R script for writing your own MCMC. Dig around to see how to use JAGS for implementation.
    
**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**


## Methods for Disclosure Risks Evaluation \#1, Tuesday 3/3/2020

### To-do (done before class on 3/3)

1. <ins>Read ```Drechsler, J. and Reiter, J. P. (2009)``` in the References folder (focus on Section 2.3 about the interval overlap utility measure), and prepare the following results.</ins>
    1. <ins>Calcuate the corresponding interval overlap measure for each of the analysis-specific utility measures you have done in Item 2.ii from the 2/25 to-do list.</ins>

2. <ins>Read ```Hu, J. (2019)``` Section 4.2.6 in the References folder, and prepare the following results.<ins>
    1. In the datasets folder, find ```ACSdata_org.csv``` and ```ACSdata_syn.csv```.
        1. Note that these datasets exlucde the HISP variable in the ACS data dictionary, but every other variable stays the same with the same name and description.
        2. Note that in ```ACSdata_syn.csv```, the following four variables are synthesized: ```LANX, WAOB, DIS, HICOV```.
    2. <ins>Assume the known variables (by the intruder) are: ```SEX, RACE, MAR```, calculate the expected match risk, the true match rate, and the false match rate.</ins> Note that:
        1. "records with the highest match probability for the target" refers to the records sharing the same known combination.
        2. "the total number of target records" should be the total number of records in the dataset (i.e. we evaluate the identification disclosure risk for every observation).
        3. There is no package for these calculations. Work through these summaries and understand how to calculate these quantities with the ACS sample. Writing a function might be useful for automating the process.
    
3. <ins>**Present your synthesis model(s) for your project dataset(s)**. Refer to the Bayesian Synthesis Models \#1 and \#2 lectures for different synthesis models we have covered, and possibly the references in Item 5 on the 2/25 to-do list for ordered categorical data synthesis and count data synthesis. Make sure to follow the correct steps when doing sequential synthesis. Perform a couple of utility measures evaluation and include them in your writeup.</ins>

**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**


## Methods for Disclosure Risks Evaluation \#2, Tuesday 3/24/2020

### To-do (done before class on 3/24)

1. Revisit the R functions in lecture slides (S20MATH301_RiskEvaluationMethods_1.pdf) about identification risk evaluation for categorical data.
    1. In the datasets folder, find ```ACSdata_org.csv```, ```ACSdata_syn.csv```, ```ACSdata_syn1.csv```, and ```ACSdata_syn2.csv```.
        1. Note that these datasets exlucde the HISP variable in the ACS data dictionary, but every other variable stays the same with the same name and description.
        2. Note that in ```ACSdata_syn.csv```, ```ACSdata_syn1.csv```, and ```ACSdata_syn2.csv```, the following four variables are synthesized: ```LANX, WAOB, DIS, HICOV```.
    2. <ins>Assume the known variables (by the intruder) are: ```SEX, RACE, MAR```, calculate the expected match risk, the true match rate, and the false match rate.</ins>
        1. Note that ```m = 3``` in this case. You should calculate the expected match risk, the true match rate, and the false match rate for each synthetic dataset, and take the averages to get the summaries.
        2. Try writing functions to perform these calculations. Lecture slides page 26 (S20MATH301_RiskEvaluationMethods_1.pdf) includes recommendations about how to update the provided functions for ```m > 1```.
 
2. <ins>Design your own identification disclosure risk measure and evaluation for continuous outcome. Do that for your CE synthesis, where ```log(Income)``` is synthesized. Prepare **a few slides of your method and your results**.</ins>

3. <ins>**Present your synthesis model(s) and utility evaluation for your project dataset(s)**.</ins>

**Make sure to use an R script / R Markdown file to document your work and bring your laptop to class. Also, write down any questions / comments you have and bring them to class for discussion.**
