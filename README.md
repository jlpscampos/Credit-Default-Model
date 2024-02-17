# Credit Default Model


Credit score models compute the probability of default and compose one of the main tools assessed by many companies to grant or deny credit for people or other companies. Generaly, based in some features and business rule, the predictive model is performed and clients who have high default score are registered in a block list and possibly have their credit application denied or revised. These kind of models are used before publicitaries campaings about credit card and other banking products to adress to target clients as well. So, the primary objective of this case is to build a predictive model to classify possible clients that can default and to understand their profiles. With only 70% of valid data, exploratory data analysis shows us that about 5% of clients are in default and through the use of a binomial model with logistic link, we quantified the effect of covariates in the target as odds ratio. Prediction was performed training a Random Forest Model composed by 400 trees with maximum depth of 4 levels, using SMOTE oversampling the less representative category of the target. Weighting the confusion matrix following business rules, we obtain an accuracy of 0.86 and recall score of 0.64.

---

## Results

From binomial regression model (Analytics.ipynb) we found the following:

* Each 10% of utilization of insecure credit lines, the odds of default increases by 53%;
* Each 5 years in increasing of age, the odds of default decreases by 15%;
* Each 1% in increasing of debt ratio assets represents an increase in odds of default by 8%;
* The odds of default incresases by 89%, each time that the client had been in default bewteen 30 and 59 days;
* The odds of default incresases by 200%, each time that the client had been in default bewteen 60 and 89 days;
* The odds of default incresases by 255%, each time that the client had been in default greater than 90 days;
* Each real state loan increases the odds of default by 7%;
* Each open credit line increases the odds of default by 4%;
* Each $1k in monthly earnings decreases the odds of default by 8%.

For Prediction (Predictive.ipynb), we found that the most important variables are:

* Monthly Wage with importance of 35%;
* Number of defaults greater than 90 days, with importance of 25%;
* Open credit lines, with 16%;
* Utilization of insecure credit lines, with 14%
* Number of defaults between 60 and 89 days, with 6%;
* Number of real state loans, with 2%;
* Age, with 1%
* Number of defaults between 30 and 59 days, Number of dependents and ratio debt assets, with bellow 1%.
