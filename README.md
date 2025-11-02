# Chi-square Analysis of Direct Marketing Campaign of Portuguese Banking Institution

## Introduction

A bank is a finacial institution that accepts deposits, lends money and provide other money-related services. In the modern financial landscape, customer acquisition and retention remain central to the sustainability of banking institutions. With the increasing availability of customer data and advancements in analytics, direct marketing has evolved into strategic tool that enables banks to deliver highly targeted and personalised offers. Among such efforts, campaigns promoting term deposit subscriptions have gained prominence, as they serve both to strengthen customer loyalty and to stabilize the bank's funding base.
## Data and Data Sourced
This report examines a direct marketing campaign conducted by a Portuguese banking institution aimed at encouraging customers to subscribe to a term deposit product. The campaign was executed primarily through telephone calls, where marketing agents contacted both existing and potential customers to present the investment offer. The dataset sourced from the UCI Machine Learning Resipository comprises detailed information on client demographics, socioeconomics characteristics, financial behavior and the outcomes of previous campaign
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

- `Test`
 The Chi-square statistic is calculated as:
 **χ<sup>2</sup> = Σ [(O<sub>i</sub> − E<sub>i</sub>)<sup>2</sup> / E<sub>i</sub>]**

Where:  
- **Σ** = Summation for all categories  
- **O<sub>i</sub>** = Observed frequency for category *i*  
- **E<sub>i</sub>** = Expected frequency for category *i*
- **E<sub>i</sub> = (Row Total × Column Total) / Grand Total**
## `Analysis`
- Determine whether the marketing campaign can be considered a successfull one(if 60% or more of client subscribe to Term Deposit)

Hypothesis:
H<sub>0</sub>: 60% or more clients subscribe to term deposit (success).
H<sub>1</sub>: 60% or more clients did not subscribe to term deposit (Failure).
