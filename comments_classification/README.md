# Comments classification  

## Task  
The online store launches a new service. Now users can edit and supplement product descriptions, just like in wiki communities. That is, clients propose their edits and comment on the changes of others. The store needs a tool that will look for toxic comments and submit them for moderation.

We have at our disposal a dataset with markup on the toxicity of edits.
It is necessary to train the model to classify comments into positive and negative.

Build a model with a quality metric F1 value of at least 0.75. 

## Data  
We have at our disposal a dataset with markup on the toxicity of edits.
The `text` column contains the text of the comment, and `toxic` is the target feature.

## Used libraries  
numpy, pandas, spacy, re, nltk, sklearn, catboost
