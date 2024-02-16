# Credit Default Model


Credit score models compute the probability of default and compose one of the main tools assessed by many companies to grant or deny credit for people or other companies. Generaly, based in some features and business rule, the predictive model is performed and clients who have high default score are registered in a block list and possibly have their credit application denied or revised. These kind of models are used before publicitaries campaings about credit card and other banking products to adress to target clients. So, the primary objective of this case is to build a predictive model to classify possible clients that can default and to understand the profile of clients in default. With only 70% of valid data, exploratory data analysis shows us that about 5% of clients are in default and through the use of a binomial model with logistic link, we quantified the effect of covariates in the target as odds ratio. Prediction was performed training a Random Forest Model composed by 400 trees with maximum depth of 4 levels, using SMOTE oversampling the less representative category of the target. Weighting the confusion matrix following business rules, we obtain an accuracy of 0.86 and recall score of 0.64.

---

From business rules and variables available in our data base the following variables were selected to be used:

| Variable Long Name | Variable Short Name | Description |
|---|---|---|
| Default | **Default** | Whether client is in default 1, otherwise 0 |
| Utilization of Insecure Credit Lines | **UIL** | Credit Risk (0-1) |
| Age | **age** | Client's age |
| Debt ratio | **RDW** | Ratio between Debt and Assets |
| Monthly Wage | **MW** | Monthly Wage |
| Default 30-59 | **NTD3059** | Number of times wherein the client was in default between 30 and 59 days |
| Default 60-89 | **NTD6090** | Number of times wherein the client was in default between 60 and 89 days |
| Default 90 | **NTDGT90** | Number of times wherein the client was in default greater or equal than 90 days |
| Numbers of loans | **NB** | Current number of real state loans |
| Number of dependents | **ND** | Current Number of dependents on income tax |
| Open Credit Lines | **OCL** |  Number of open credit lines |
