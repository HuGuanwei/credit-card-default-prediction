#### Attribute Information:

This research employed a binary variable, default payment (Yes = 1, No = 0), as the response variable. This study reviewed the literature and used the following 23 variables as explanatory variables: 

`X1`: Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit. 

`X2`: Gender (1 = male; 2 = female). 

`X3`: Education (1 = graduate school; 2 = university; 3 = high school; 4 = others). 

`X4`: Marital status (1 = married; 2 = single; 3 = others). 

`X5`: Age (year). 

`X6 - X11`: History of past payment. We tracked the past monthly payment records (from April to September, 2005) as follows: 

`X6` = the repayment status in September, 2005; `X7` = the repayment status in August, 2005; . . .;`X11` = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above. 

`X12-X17`: Amount of bill statement (NT dollar). `X12` = amount of bill statement in September, 2005; `X13` = amount of bill statement in August, 2005; . . .; `X17` = amount of bill statement in April, 2005. 

`X18-X23`: Amount of previous payment (NT dollar). `X18` = amount paid in September, 2005; `X19` = amount paid in August, 2005; . . .;`X23` = amount paid in April, 2005. 



#### Categorical Features Exploration

<img src="visualization\categorical.png"  style="zoom:70%" />



#### Parallel Coordinates Visualization 

<img src="visualization\parallel_coordinates (1).png"  style="zoom:60%" />



#### Correlation Matrix

<img src="visualization\corr.png"  style="zoom:80%" />

Note correlation coefficients between `PAY_i` and `PAY_j`, `BILL_AMTi` and `BILL_AMTj`.

`BILL_ATMi` (i>=2) have little linear relation to the target but they are highly correlated. Thus we can drop them.



#### Data Preprocessing

1. one-hot encoding for categorical features
2. handle imbalanced data: oversampling
3. min-max rescaling for neural network model only



#### Model

1. Tree-based Adaptive Boosting
2. Random Forest
3. Neural Network
4. Ensemble 



#### Performance
<img src="visualization\performance.png"  style="zoom:80%" />



#### Relevant Papers:

Yeh, I. C., & Lien, C. H. (2009). The comparisons of data mining techniques for the predictive accuracy of probability of default of credit card clients. Expert Systems with Applications, 36(2), 2473-2480.
