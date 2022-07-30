# Profitability study of mobile operator tariffs
## Data
Input data - a sample of data from 500 clients of a mobile operator for 2018:  

Table `users` - information about users:  
  * `user_id` - unique user ID  
  * `first_name` - username  
  * `last_name` — user last name  
  * `age` - user age (years)  
  * `reg_date` — tariff connection date (day, month, year)  
  * `churn_date` - the date when the tariff was discontinued (if the value is omitted, it means that the tariff was still in effect at the time the data was uploaded)  
  * `city` — user's city of residence  
  * `tarif` — tariff plan name  

Table `calls` - information about calls:  
  * `id` — unique call number  
  * `call_date` — call date  
  * `duration` — call duration in minutes  
  * `user_id` - ID of the user who made the call  

Table `messages` - information about messages:  
  * `id` — unique call number  
  * `message_date` — message date  
  * `user_id` - ID of the user who sent the message  

Table `internet` - information about Internet sessions:  
  * `id` — unique session number  
  * `mb_used` - the amount of Internet traffic spent per session (in megabytes)  
  * `session_date` — internet session date  
  * `user_id` - user ID  

Table `tariffs` - information about tariffs:  
  * `tariff_name` — tariff name  
  * `rub_monthly_fee` — monthly subscription fee in rubles  
  * `minutes_included` - the number of minutes of conversation per month included in the subscription fee  
  * `messages_included` - the number of messages per month included in the monthly fee  
  * `mb_per_month_included` - the amount of Internet traffic included in the subscription fee (in megabytes)  
  * `rub_per_minute` - the cost of a minute of conversation in excess of the tariff package (for example, if the tariff includes 100 minutes of conversation per month, then a fee will be charged from 101 minutes)  
  * `rub_per_message` - the cost of sending a message in excess of the tariff package  
  * `rub_per_gb` - the cost of an additional gigabyte of Internet traffic in excess of the tariff package (1 gigabyte = 1024 megabytes)  

## Task
Analyze customer behavior and conclude which tariff brings more revenue.

## Used libraries
pandas, scipy
