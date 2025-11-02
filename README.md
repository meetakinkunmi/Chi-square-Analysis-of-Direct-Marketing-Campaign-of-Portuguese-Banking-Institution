# Chi-square Analysis of Direct Marketing Campaign of Portuguese Banking Institution

## Introduction

A term deposit is a low-risk investment where customer deposit a certain amount of money for a fixed period in exchange for a guaranteed interest rate. Banks market term deposits extensively because these accounts offer them essential benefits. Marketing term deposits helps banks attract new customers, build customer loyalty by providing a safe investment option, and meet regulatory capital and funding stability requirements.
## Data and Data Source
This report examines a direct marketing campaign conducted by a Portuguese banking institution aimed at encouraging customers to subscribe to a term deposit product. The campaign was executed primarily through telephone calls, where marketing agents contacted both existing and potential customers to present the investment offer. The dataset was sourced from the UCI Machine Learning Resipository(https://archive.ics.uci.edu/dataset/222/bank+marketing) and it comprises detailed information on client demographics, socioeconomics characteristics, financial behavior and the outcomes of previous campaign
## Objectives
The general objective of this analysis is to identify variables statistically significant affecting customers' likelihood of subscription, while the specific objective is to:
- Determine whether the marketing campaign can be considered a successfull one(if 60% of client subscribe to Term Deposit)
- Determine if there is association between the job type of clients and clients subscribing to Term Deposit
- Determine if there is association between the marital status of clients and clients subscribing to Term Deposit
- Determine if there is association between the educaion background of clients and clients subscribing to Term Deposit
## Methodology - Chi-square Analysis
Chi-square analysis is a statistical method used totest relationships between caterical variables by comparing observed data to expected outcomes. It helps determine wheter differences or associations are statistically significant or due to chance.
- There are two types of Chi-Square Tests
1. `Chi-square Goodness of Fit Test` - Tests if a single categorical variable fits a theoretical distribution. For the purpose of this report, chi-square goodness of fit will be used to achieve objective one.
2. `Chi-square Test of Independence` - Tests if two categorical variables are related. For the purpose of this report, chi-square test of independence will be used to achieve every other objectives except the first one.

The Chi-square statistic is calculated as:

 **χ<sup>2</sup> = Σ [(O<sub>i</sub> − E<sub>i</sub>)<sup>2</sup> / E<sub>i</sub>]**

Where:  
- **Σ** = Summation for all categories  
- **O<sub>i</sub>** = Observed frequency for category *i*  
- **E<sub>i</sub>** = Expected frequency for category *i*
- **E<sub>i</sub> = (Row Total × Column Total) / Grand Total**

## `Analysis`
1. Determine whether the marketing campaign can be considered a successfull one(if 60% or more of client subscribe to Term Deposit)

- `Hypothesis:`

H<sub>0</sub>: 60% or more clients subscribe to term deposit (success).

H<sub>1</sub>: 60% or more clients did not subscribe to term deposit (Failure).

- `Decision rule:` Accept the null hypothesis if p-value < 0.005, otherwise we fail to accept.

![Sample Plot](plots/subs_plot.png)
Fig. 1: How cliets subscribe to Term Deposit after the campaign.

Table 1: Can the campaign be considered a successful one?

|Statistic  |Chi-Square Goodness of Fit |
|:---------:|:-------------------------:|
|Chi-Square	|15088.719298               |
|Asymp. Sig.|0.00                       |


- Decision: Since p-value (0.00) < 0.05, we therefore fail to accept the null hypothesis and conclude that 60% or more clients did not subscribe to Term Deposit after the campaign.

