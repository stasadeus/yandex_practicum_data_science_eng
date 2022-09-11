# Model for predicting the churn of bank customers
## Data
Clients started leaving the bank. Every month. A little, but noticeable. Banking marketers figured it was cheaper to keep current customers than to attract new ones.
We have been provided with historical data on customer behavior and termination of agreements with the bank.
Data Source: [https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling](https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling) 

**Data Description**

*Features*

- `RowNumber` - row index in the data
- `CustomerId` - unique customer ID
- `Surname` - surname
- `CreditScore` - credit rating
- `Geography` - country of residence
- `Gender` - gender
- `Age` - age
- `Tenure` - how many years a person has been a client of the bank
- `Balance` - account balance
- `NumOfProducts` - the number of bank products used by the client
- `HasCrCard` - the presence of a credit card
- `IsActiveMember` - client activity
- `EstimatedSalary` - estimated salary

*Target feature*

- `Exited` - the fact that the client left

## Task
Build a model with the largest possible value of the F1-measure for the classification problem, which, after analyzing the behavior of customers, will predict whether the customer will leave the bank in the near future or not.

## Used libraries
pandas, missingno, matplotlib, sklearn
