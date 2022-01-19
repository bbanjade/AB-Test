# AB-Test
##### The two files analyze same dataset, one using R-Studio, and another using Python.
##### The problem of these projects are trying to test the impact of a new product page, designed by a company, on the effectiveness of customer purchase. Company providing this data has a product page which has conversion rate of 13%, and management wants to increase the rate to 15% by doing some minor changes in the product page, thereby creating a new page. So, these projects are checking if there is at least 2% statistical difference between the two page. Both analysis rejected the effectiveness of the new page by performing a simple ab-test. Both codes in R & Python are included in the folder, the codes/analysis in Python are as follows:

# 1) AB-Test in Python:

 5 steps of this Analysis:
##### 1. Experiment Definition
##### 2. Data collection and preparation
##### 3. Visualization
##### 4. Hypothesis testing
##### 5. Conclusions

#### 1. EXPERIMENT DEFINITION
##### The data is related with an online e-commerce business, they are doing some changes in the website and want to see if the new website helps to convert customer to purchaser. Current conversion rate is 13%, if there is an increase 2%, then the effectivness of new webpage will be justified. So, with new website 15% conversion rate needs to be created. So, we are trying to test if the new webpage is better than the old one, but we don't know either it is better or worst. So, we are doing tow-tailed test:

### H0: p = p0
### H1: p != p0

##### p & p0 are the conversion rate of the new and old design. 

##### Our confidence level is 95%: a = 0.05, which means “if the probability of observing a result as extreme or more (p-value) is lower than α, then we reject the Null hypothesis”. (or a = 0.05 means 5% probability with confidence of (1 - a) of 95%.)

#### Define variables
##### Control group - group of customers shown the old design.
##### Treatment group - group of customers shown the new design.

##### Our dependent variable (i.e., our target measurement) is the conversion_rate, which is a binary variable: 0 means user did not buy the product and 1 means user bought the product.

##### sample size for each group is calculated from the "Power Analysis", which depends on: (a) Power of test (1-B) -- probability of finding a statistical difference between the groups in test set when a difference is actually present. This is usually set at 0.8 by convention. (b) Alpha value (a) - The critical value set at 0.05. (c) Effect size -- How big of a difference we expect there to be between teh conversion rates.

##### we need a difference of 2%, so we need to use 13% and 15% to calculate the effect size we want. Rest Python will caclculate.
