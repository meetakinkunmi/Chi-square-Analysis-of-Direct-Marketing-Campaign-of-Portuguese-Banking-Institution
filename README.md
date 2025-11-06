# Chi-square Analysis of Direct Marketing Campaign of Portuguese Banking Institution

## Introduction
A term deposit is a low-risk investment where customer deposit a certain amount of money for a fixed period in exchange for a guaranteed interest rate which it's equivalent amount from the initial deposit will given to the customer on a monthly basis or at an agreed time frame. Banks market term deposits extensively because these financial products offer the bank important benefits. Marketing term deposits helps banks attract new customers, build customer loyalty by providing a safe investment option, and meet regulatory capital and funding stability requirements.
## Data and Data Source
This report examines a direct marketing campaign conducted by a Portuguese banking institution aimed at encouraging customers to subscribe to a term deposit product. The campaign was executed primarily through telephone calls, where marketing agents contacted both existing and potential customers to present the investment offer. The marketing campaign dataset was sourced from the UCI Machine Learning Resipository(https://archive.ics.uci.edu/dataset/222/bank+marketing) and it comprises detailed information on customers demographics or social status, socioeconomics characteristics, financial behavior, the outcomes of previous campaign and the final actions of each customers whether subscribed or not.
## Objectives
The general objective of this analysis is to establish whether social status of customers can statistically and significantly influence their decision in making Term Deposit, while the specific objective is to:
- Determine whether the marketing campaign can be considered a successfull one(if 60% of client subscribe to Term Deposit)
- Determine if there is an association between the job type of customers and customers subscribing to Term Deposit
- Determine if there is an association between the marital status of customers and customers subscribing to Term Deposit
- Determine if there is an association between the education background of customers and customers subscribing to Term Deposit
## Methodology - Chi-square Analysis
Chi-square analysis is a statistical method used to test relationships between caterical variables by comparing observed data to expected outcomes. It helps determine wheter differences or associations are statistically significant or due to chance.
- **There are two types of Chi-Square Tests**
1. `Chi-square Goodness of Fit Test` - Tests if a single categorical variable fits a theoretical distribution. For the purpose of this report, chi-square goodness of fit will be used to achieve objective one.
2. `Chi-square Test of Independence` - Tests if two categorical variables are related. For the purpose of this report, chi-square test of independence will be used to achieve every other objectives except the first one.

The Chi-square statistic is calculated as:

$$
X^2 = \sum_{i=1}^{n} \frac{(Obs_i - Exp_i)^2}{Exp_i}    
$$

Where:  

- $\sum$ = Summation for all categories  
- $Obs_i$ = Observed frequency for category *i*  
- $Exp_i$ = Expected frequency for category *i*

$$
Exp_i = \frac{Row_{Total} * Column_{Total}}{Grand_{Total}}
$$

- **Level of Significance = 0.05**

- **Decision rule for hypothesis:** Accept the null hypothesis if p-value < 0.05, otherwise we fail to accept the null hypothesis.

## Analysis - Objective Based

**Objective 1:** Determine whether the marketing campaign can be considered a successfull one(if 60% or more of client subscribe to Term Deposit)

**Hypothesis:**

- H<sub>0</sub>: 60% or more customers subscribe to term deposit (success).

- H<sub>1</sub>: 60% or more customers did not subscribe to term deposit (Failure).

![Sample Plot](plots/subs_plot.png)

**Fig. 1: How customers subscribed to Term Deposit after the campaign**

**Table 1: Can the campaign be considered a successful one?**

|Statistic  |Chi-Square Goodness of Fit |
|:---------:|:-------------------------:|
|Chi-Square	|15088.719298               |
|Asymp. Sig.|0.00                       |


- **Decision:** Since p-value (0.00) < 0.05, we therefore fail to accept the null hypothesis and conclude that 60% or more customers did not subscribe to Term Deposit after the campaign. That is, based on the objective of this analysis, the marketing campaign can be considered an unsuccessful one.

**Objective 2:** Determine if there is an association between the job type of customers and customers subscribing to Term Deposit

**Hypothesis:**

- H<sub>0</sub>: There is no association between the job type of customers and subscribing to Term Deposit

- H<sub>1</sub>: There is association between the job type of customers and subscribing to Term Deposit

![Sample Plot](plots/obj2_plot1.png)

**Fig. 2: Customers with which job type should marketing agents focus their attention in the coming campaign?**

**Table 2: Does job type influences customer decision to subscribe?**

|               |chi-square test    |
|:-------------:|:-----------------:| 
|statistic      |8.361055e+02       |
|p-value        |3.337122e-172      |
|df             |1.100000e+01       |

- **Decision:** Since p-value ($X^2 = 836.11$, df=11, p-value=0.00) < 0.05, we therefore fail to accept the null hypothesis and conclude that there is an association between the job type of customers and their decision to subscribe to Term Deposit. This shows that job type can significantly influence customer decision to subscribe to term deposit.

**Objective 3:** Determine if there is an association between the marital status of customers and subscribing to Term Deposit

**Hypothesis**

- H<sub>0</sub>: There is no association between marital status of customers and subscribing to Term Deposit

- H<sub>1</sub>: Tere is an association between marital status of customers and subscribing to Term Deposit

![Sample Plot](plots/obj3_plot1.png)

**Fig. 3: How customers subscribed to Term Deposit by marital status**

**Table 3: Does customer's marital status matters in their decision to subscribe to Term Deposit?**

|               |chi-square test    |
|:-------------:|:-----------------:| 
|statistic      |196.4959           |
|p-value        |0.0000             |
|df             |2.0000             |

- **Decision:** Since p-value (0.00) < 0.05, we therefore fail to accept the null hypothesis and conclude that there is an association between marital status of customers and customer's decision to subscribe to Term Deposit. This shows that, marital status of customers can significantly influence their decisions in making term deposit.

4. Determine if there is an association between the education background of background of customers and subscribing to Term Deposit

**Hypothesis:**

- H<sub>0</sub>: There is no association between educational level of customers and subscribing to Term Deposit

- H<sub>1</sub>: Tere is an association between educational level of customers and subscribing to Term Deposit

![Sample Plot](plots/obj4_plot.png)

**Fig. 4: How education level influences customers decision to subscribing to Term Deposit**

**Table 4: Does Educational level significantly influences customers decision to subscribe to Term Deposit**

|               |chi-square test    |
|:-------------:|:-----------------:| 
|statistic      |238.9235           |
|p-value        |0.0000             |
|df             |3.0000             |

- **Decision:** Since p-value (0.00) < 0.05, we therefore fail to accept the null hypothesis and conclude that there is an association between marital status of customers and customer's decision to subscribe to Term Deposit. Therefore, we can conclude that education level of customers can statististically and significantly influence their decisions to making term deposit.

## Conclusion

Term Deposit can be referred to as a financial product where a customer commits a certain amount of money for a fixed or predetermined period in exchange for a fixed exchange rate. It is no secret that banks benefit a great deal from such deposits as it would solidify the bank competitive strength and further supply and stabilize bank's capital available for running of the business. The main objective of this analysis is to determine whether social status of customers can influence their decision in making term deposit for a specific period of time. Using Direct Marketing Campaign of Portuguese Banking Institution dataset which contains 45,211 data points. To test the set forth hypothesis of this report, chi-square test is adopted to test the theoratical distribution of customers decision in subscribing to term deposit and figuring factors that influence such decision among the selected social status indicators.

Out of 45,211 customers and potential customers that marketing agents in a Portuguese Banking Institution marketed the term deposit finacial product to, a staggering 39,922 (88% approx.) did not eventually subscribe while 5,289 (11% approx.) subscribed at the end of the campaign to term deposit. Therefore, this campaign can be considered an unsuccessful campaign according to the target from objective one of this analysis.

 Chi-square test reveals that 