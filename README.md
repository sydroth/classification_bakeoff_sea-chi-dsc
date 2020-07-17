# Bake Off

![Baking](https://media.giphy.com/media/WvRgv9DdgJtPcIlTEI/giphy.gif)

## Challenge 

The Bake Off challenge is a Kaggle-like format where you are given a set of data and tasked with building your best model on a set of training data. To do so, you employ all of the skills you have learned over the course: data cleaning, EDA, feature engineering/transformation, feature selection, hyperparameter tuning, and model evaluation.  Once you have settle on a model that performs to your standards, you apply that model to a set of test features.  You are not given the labels, so you only know how well your model performed until the challenge is over. This type of setup is not limited to Kaggle.  Groups who chose the Tanzanian well data had a similar set up.  The technical challenge portion of job interviews make take this form as well.  While the focus is on prediction, and there is a time limit, try to maintain some semblence of your workflow's process by adding appropriate markdown to your working notebook.  We will ask you to push your notebooks at the end.  While they won't be graded, your peers will appreciate insight into how you achieved your score. 

The goal for this challenge is to predict whether a person will **default** on their loan. 
The dataset comes from customers default payments in Taiwan.

## Data Files

In this repo, you will find two csv files:

1. `train_data.csv`
This includes the features and target variables that you will use to train a predictive model

2. `test_features.csv`
This includes a testing set of data with the `defualt payment next month` column removed. You will make your final predictions on these observations and submit the predictions as a csv file.

## Feature Descriptions

* ID: ID of each client
* LIMIT_BAL: Amount of given credit in NT dollars (includes individual and family/supplementary credit
* SEX: Gender (1=male, 2=female)
* EDUCATION: (1=graduate school, 2=university, 3=high school, 4=others, 5=unknown, 6=unknown)
* MARRIAGE: Marital status (1=married, 2=single, 3=others)
* AGE: Age in years
* PAY_0: Repayment status in September, 2005 (-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, … 8=payment delay for eight months, 9=payment delay for nine months and above)
* PAY_2: Repayment status in August, 2005 (scale same as above)
* PAY_3: Repayment status in July, 2005 (scale same as above)
* PAY_4: Repayment status in June, 2005 (scale same as above)
* PAY_5: Repayment status in May, 2005 (scale same as above)
* PAY_6: Repayment status in April, 2005 (scale same as above)
* BILL_AMT1: Amount of bill statement in September, 2005 (NT dollar)
* BILL_AMT2: Amount of bill statement in August, 2005 (NT dollar)
* BILL_AMT3: Amount of bill statement in July, 2005 (NT dollar)
* BILL_AMT4: Amount of bill statement in June, 2005 (NT dollar)
* BILL_AMT5: Amount of bill statement in May, 2005 (NT dollar)
* BILL_AMT6: Amount of bill statement in April, 2005 (NT dollar)
* PAY_AMT1: Amount of previous payment in September, 2005 (NT dollar)
* PAY_AMT2: Amount of previous payment in August, 2005 (NT dollar)
* PAY_AMT3: Amount of previous payment in July, 2005 (NT dollar)
* PAY_AMT4: Amount of previous payment in June, 2005 (NT dollar)
* PAY_AMT5: Amount of previous payment in May, 2005 (NT dollar)
* PAY_AMT6: Amount of previous payment in April, 2005 (NT dollar)
* default.payment.next.month: Default payment (1=yes, 0=no)


## Instructions
- Every team member fork and then clone this repo onto your computer. Figure out a strategy for how to collaborate, which may look like selecting one team member as the primary "coder".  We leave it to you to set-up a productive team dynamic, but keep in mind, the deliverable of this exercise is one csv file.   
- Load up a Jupyter and start CRISP'ing.
- The instructions for this bakeoff are limited with regards to modeling. Go wild. Use any model you want.  Feature engineer your head off.
- Once you are satisfied with your model, or you find time running out, use the `test_features.csv` to predict a 0 or 1 signifying whether the individual defaulted on their loan.  See Submission guidelines below. 
- Please be sure to use your own work.  If you have worked on this dataset before, don't copy and paste your previous work. Obviously there is no way that we can ask you not to use past experience, but we can ask you not to use past code.



## Submissions
Save your predictions in a .csv file with the following pattern. 
- `credit_default_preds_yourteaminitials.csv`
- For example, if Joél and Erin were a team, their submission would look like `credit_default_preds_jceh.csv`

- There are different ways to turn arrays to .csv's.  You can use any method you choose, but be sure your submission has no heading, no index and one column. Your submission must match the number of records in the `test_features.csv`. Don't worry about rounding.  A valid submission could look like below. 

0<br>
0<br>
1<br>
1<br>
...

- You will be given until **3 pm** CT/**1 pm** PT to submit to build your best model using the training data. Any late submissions will not be considered. 
- We would usually cut you off after 3 hours, but we are giving you 4.5 hours so that you can attend  lunch hour with [Brad's Deals](https://www.bradsdeals.com/?acq=true&v=onboarding&utm_source=Google&utm_medium=Search&utm_campaign=preferencedbasedonboarding&utm_content=interestmanagement&c_id=4347&s=Google|Search|preferencebasedonboarding|interestmanagement&gclid=EAIaIQobChMIvOe7hKjU6gIVUvDACh2_Mg8OEAAYASAAEgK6b_D_BwE). 
- Slack your .csv file to the `chicago-seattle-ds051120` channel before time is up. Any submissions after the deadline will be evaluated, but not included in the judging.

## Metrics
Test results will be scored by F1-score. The group which submitted the predictions with the highest F1-score will be announced Monday morning. As a reward, they will receive a round of applause. 

## Share
- After submission, push your repo with your work to your forked repo. In this way, your peers will be able to gain valuable wisdom from the different tactics employed.

