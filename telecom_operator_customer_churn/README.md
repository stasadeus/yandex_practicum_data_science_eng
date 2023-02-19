# Forecasting the outflow of customers of a telecom operator 

## Task  
A telecom operator wants to learn how to predict customer churn. If it turns out that the user plans to leave, he will be offered promotional codes and special conditions. The operator's team collected personal data about some customers, information about their tariffs and contracts.  
It is necessary to predict whether the client will leave the telecom operator in the near future or not. We have been provided with personal data about some customers, historical data on their behavior and termination of contracts with a telecom operator. It is necessary to build a model with an AUC-ROC metric value of at least 0.85.

## Data
The data consists of files obtained from various sources:  

- `contract.csv` - information about the contract;  
- `personal.csv` - personal data of the client;  
- `internet.csv` - information about Internet services;  
- `phone.csv` - information about telephony services.  

In all files, the `customerID` column contains the customer ID.  
Information on contracts is current as of February 1, 2020  

*Target feature*  

- The fact that the client left  

## Used libraries
numpy, pandas, matplotlib, seaborn, phik, sklearn, catboost, lightgbm
