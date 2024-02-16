# Credit Default Model

Credit score models compute the probability of default and compose one of the main tools assessed by many companies to grant or deny credit for people or other companies. Generaly, based in some features and business rule, the predictive model is performed and clients who have high default score are registered in a block list and possibly have their credit application denied or revised. This kind of model are used before publicitaries campaings about credit card and other banking products to adress to target clients.

So, the primary objective of this case is to build a predictive model to classify possible clients that can default and to understand the profile clients in default.

---

From business rules and variables available in our data base the following variables were selected to be used:

| Variable Long Name | Variable Short Name | Description |
|---|---|---|
| Default | **Default** | Whether client is in default 1, otherwise 0 |
| Utilization of Insecure Credit Lines | **UIL** | Credit Risk (0-1) |
| Age | **age** | Client's age |
| Debt ratio | **RDW** | Ratio between Debt and Assets |
| Monthly Wage | **MW** | Monthly Wage |
| Default 30-59 | **NTD3059** | Number of times wherein the client was in default from 30 to 59 days |
| Default 60-89 | **NTD6090** | Number of times wherein the client was in default from 60 to 89 days |
| Default 90 | **NTDGT90** | Number of times wherein the client was in default greater or equal than 90 days |
| Numbers of loans | **NB** | Current number of real state loans |
| Number of dependents | **ND** | Current Number of dependents on income tax |
| Open Credit Lines | **OCL** |  Number of open credit lines |
