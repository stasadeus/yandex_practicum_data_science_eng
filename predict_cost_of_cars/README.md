# Determining the cost of cars

## Task
A used car service is developing an app to attract new customers. In it, you can quickly find out the market value of your car. We have historical data at our disposal:   technical characteristics, configurations and prices of cars. You need to build a model to determine the cost. The customer is important:

- prediction quality;
- prediction speed;
- training time.  

## Data

**Data Description**  

Features  

- DateCrawled - date of downloading the questionnaire from the database  
- VehicleType - type of car body  
- RegistrationYear — year of vehicle registration  
- Gearbox - type of gearbox  
- Power - power (hp)  
- Model - car model  
- Kilometer - mileage (km)  
- RegistrationMonth - month of car registration  
- FuelType — type of fuel  
- Brand - car brand  
- Repaired - was the car under repair or not  
- DateCreated - date of creation of the questionnaire  
- NumberOfPictures - the number of photos of the car  
- PostalCode - postal code of the owner of the profile (user)  
- LastSeen - date of last user activity  
Target feature  

Price - price (euro)

## Libraries used  
numpy, pandas, missingno, matplotlib, seaborn, sklearn, lightgbm, catboost
