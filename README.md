# Project 1: German Bank Credit Risk
Author: Amin

## Problem Statement

A german bank wanted to study its list of clientele and determine what factors influenced whether an individual would become a good or bad risk. 

It wanted to come up with a profile of its clients, particularly those of bad risks, in hopes of managing their risk better. Furthermore, in getting this profile, they wanted to see if they could apply this profile to existing clients to predict if they would be a good or bad risk. 

As part of a team that does analysis for the banking industry, this project seeks to understand and determine the client profile for this bank that would influence the type of risk they fall under. In addition to that, this project also seeks to come up with a model to assist the bank in predictive analysis. These two goals would allow the bank to maximize their profits by better management of their risks. 

## About Dataset

This dataset consist of 1000 records of individuals with 9 features + target.  

**Features**:  

1. Age | Age of clients | Integer | Years  
2. Sex | Gender of clients | String | Days  
3. Job | Job Type of clients | Integer | 0: Unskilled & non-resident / 1: Unskilled and resident / 2: Skilled / 3: Highly skilled  
4. Housing | Housing Type of clients | String | Own / Rent / Free  
5. Saving accounts | Savings Account Balance of clients | String | Little / Moderate / Quite Rich / Rich    
6. Checking account | Checking Account Balance of clients | String | Little / Moderate / Rich    
7. Credit amount | Credit Amount of clients | Integer  
8. Duration | Duration in months | Integer  
9. Purpose | Purpose for clients | String | Car / Furniture/Equipment / Radio/TV / Domestic Appliances / Repairs / Education / Business / Vacation/Others  
10. Risk | Target Variable | String | Binary: Good / Bad

**Data Source**: https://www.kaggle.com/uciml/german-credit  


## Objectives: 

1) Determine the client profile of those with and without a good or bad risk based on features available.  

2) Create a model that would be able to predict whether an individual is a good or bad risk.  


## Conclusion  

**Objectives**:  

1) Determine the client profile of those with good and bad risk.  

- **Age**: Across all other variables, those that are older generally tend to be a good risk as opposed to younger individuals.  

- **Credit amount**: Generally tends to be lower for good risk when compared with other variables. 

- **Duration**: Also generally tends to be lower for good risk when compared with other variables. Good risks are mostly when durations are below 20 months, while those above are mostly bad risk.  

- **Gender**: Males tend to be better risk as compared to females.  

- **Job Type**: Unskilled & non-resident, unskilled & resident, and skilled individuals tend to be better risk as compared to highly skilled ones.  

- **Housing Type**: Individuals who owns their housing tends to be better risk than those whose housing is either free or rent.  

- **Checking Account**: Those who are classified as little & rich checking account had better risk as compared to those with moderate.  

- **Saving Account**: Those who are classified as little, quite rich & rich saving account had better risk as compared to those with moderate.  

- **Purpose**: Those for the purpose of cars, furniture/equipment & radio are better risk than those of business, domestic appliances, repairs, education & vacation/others.  


2) Create a model that would be able to predict whether a client is a good or bad risk.  
- **XGBoost** is the best model out of all for the prediction of cardiovascular disease.  

    - **Recall** is our more important metric since we wanted to focus more on being able to detect bad risks. XGBoost had the best at 0.37  
    - Has an **accuracy** of 0.72  
    - Has a **precision** of 0.54  
    - Has a **f1-score** of 0.44  
    - Has an **ROC AUC** of 0.62  


Next Steps: 

1) Further tuning of our hyperparameters needed.  
    - Results gotten is far from good.  

2) Apply SMOTE technique to our dataset.  
    - Our data is imbalanced with 70% being good risk, while the remainder were bad risk.  
