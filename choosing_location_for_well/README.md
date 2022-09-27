# Choosing a location for a well
## Data
The customer, a mining company, provided exploration data from three regions. 

**Data Description**

*Features*

- id - unique identifier of the well;
- f0, f1, f2 - three signs of points (it doesn't matter what they mean, but the signs themselves are significant);

*Target feature*

- `Exited` - the fact that the client left

Synthetic data: details of contracts and characteristics of deposits were not disclosed.

## Task
Build a machine learning model that will help a mining company determine the region where to drill a new well so that production brings the greatest profit.
Assess possible profit and risks.
- Only linear regression is suitable for training the model (the rest are not predictable enough).
- When exploring the region, 500 points are explored, from which, using machine learning, the best 200 are selected for development.
- The budget for the development of wells in the region is 10 billion rubles.
- At current prices, one barrel of raw materials brings 450 rubles of income. The income from each unit of the product is 450 thousand rubles, since the volume is indicated in thousands of barrels.
- After assessing the risks, you need to leave only those regions in which the probability of losses is less than 2.5%. Among them, choose the region with the highest average profit.

## Used libraries
numpy, pandas, matplotlib, seaborn, sklearn, scipy
