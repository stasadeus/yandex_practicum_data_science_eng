# Model for recommending mobile operator tariffs
## Data
The mobile operator found out: many customers use archival tariffs. They want to build a system that can analyze customer behavior and offer users a new tariff: "Smart" or "Ultra".
We have at our disposal data on the behavior of customers who have already switched to these tariffs.  

Each object in the data set is information about the behavior of one user per month. Known:
- `calls` - number of calls,
- `minutes` — total duration of calls in minutes,
- `messages` — number of sms messages,
- `mb_used` - used Internet traffic in Mb,
- `is_ultra` - what tariff did you use during the month ("Ultra" - 1, "Smart" - 0).

## Task
Build a model with the highest possible accuracy for the classification task, which, after analyzing the behavior of customers, will select the appropriate new tariff "Smart" or "Ultra" for the cellular operator's customers. Data preprocessing is not required - it was done in the project ["Comparison of the profitability of mobile operator tariffs"](https://github.com/stasadeus/yandex_practicum_data_science_eng/tree/main/mobile_operator_tariffs_profitability)

## Used libraries
pandas, matplotlib, sklearn
