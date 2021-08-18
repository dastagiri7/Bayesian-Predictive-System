# Bayesian-Predictive-System
## Motivation
The aim of the proposed system is to allow cleint next month deafult payment using Bayesian Logistic regression data analysis.

**Knowledge Requirements**: 
1. Bayesian inference, Machine Learning, Statistics.
2. jags.model is used to create an object representing a **Bayesian graphical model**, specified with a BUGS-language description of the prior distribution, and a set of data.
3. Markov chains (conditional independence) and Monte Carlo techniques (estimation by simulation) to yield **Markov chain Monte Carlo (MCMC)** allows us to indeirectly generate independent sample from a particular posterior distribution.

## DataSet
The dataset I have chosen is the Default of credit card clients. The dataset is mainly aimed at the default payment of customers in Taiwan. The estimated probability of default will be more valuable than the binary result of classification - credible or not credible clients.

I gathered this dataset from the UCI respository: https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients

The data set contains 23 columns and a default payment binary responce variable to be predicted. There are columns that represents the demographics of the customer like gender, marriage, education and age. The data set also provides the information about the customer's previous payments, bill amounts and payment due's that helps in predicting the default payment. 
- The columns PAY_0, PAY_2, PAY_3, PAY_4,  PAY_5, PAY_6 represents the history of past payments where PAY_0=the repayment status in September,...and PAY_6=the repayment status in April with the values ranging as  -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above respectively. 
- The columns BILL_AMT1, BILL_AMT2, BILL_AMT3, BILL_AMT4, BILL_AMT5, BILL_AMT6 represents the amount of bill statement in dollars. 
- The columns PAY_AMT1,PAY_AMT2, PAY_AMT3, PAY_AMT4, PAY_AMT5, PAY_AMT6 represnts the amount of previous payments in dollars from Septemper to April.

## Project Pipeline

1. Data Pre-processing(handling N/A values, Plotting individual for better undestanding and observations).
2. Feature engineering(Plotting the independent variable's behavior with respect to dependent variable and observe by remove based on analysis, Co-Variat).
3. Bayesian modeling(jags.model and frequentist approaches).
4. Model observation (Convergence diagnosis Analysis, autocorrelation statistics and Examine convergence of the Markov chains using the Gelman-Brooks-Rubin diagnostic).
5. Models accuracy analysis(Deviantion Information Criterion DIC metric).

## Future Plans

Integrate with Big data for larger datasets and for more samplings iterations(re-write JAGS).
