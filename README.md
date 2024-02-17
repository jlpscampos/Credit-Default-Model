# Credit Default Model

Credit score models play a crucial role in financial decision-making processes by estimating the probability of default, influencing credit approvals or denials. These models analyze various features and business rules to predict the likelihood of clients defaulting on their credit obligations. The outcomes help financial institutions identify high-risk clients, potentially leading to credit application denials or closer scrutiny. Additionally, credit models inform targeted advertising campaigns for credit cards and other banking products. This project aims to build a predictive model for classifying potential defaulting clients and gaining insights into their profiles.

Despite having only 70% valid data, exploratory data analysis revealed that approximately 5% of clients are in default. Leveraging a binomial model with a logistic link, we quantified the impact of covariates on the target variable using odds ratios. The predictive model, a Random Forest Model consisting of 400 trees with a maximum depth of 4 levels, was trained with SMOTE oversampling applied to the less representative category of the target variable. By weighting the confusion matrix according to business rules, we achieved an accuracy of 0.86 and a recall score of 0.64.

## Results

From the binomial regression model (Analytics.ipynb), we discovered the following key insights:

- A 10% increase in the utilization of insecure credit lines corresponds to a 53% increase in the odds of default.
- Each 5-year increase in age results in a 15% decrease in the odds of default.
- A 1% increase in the debt ratio to assets leads to an 8% increase in the odds of default.
- Clients in default for 30-59 days experience an 89% increase in the odds of default.
- Clients in default for 60-89 days see a 200% increase in the odds of default.
- Clients in default for more than 90 days face a 255% increase in the odds of default.
- Each real estate loan increases the odds of default by 7%.
- Each open credit line raises the odds of default by 4%.
- Each $1k increase in monthly earnings decreases the odds of default by 8%.

For predictions (Predictive.ipynb), we identified the most influential variables:

- Monthly wage, with an importance of 35%.
- Number of defaults greater than 90 days, with an importance of 25%.
- Open credit lines, with an importance of 16%.
- Utilization of insecure credit lines, with an importance of 14%.
- Number of defaults between 60 and 89 days, with 6% importance.
- Number of real estate loans, with 2% importance.
- Age, with 1% importance.
- Number of defaults between 30 and 59 days, number of dependents, and the debt assets ratio, each contributing below 1%.
