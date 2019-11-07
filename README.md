# Document De-identification
## Available data
First data set comes from [2006 i2b2](https://www.i2b2.org/NLP/DataSets/Main.php) 

Second data set comes from [2014 n2c2](https://n2c2.dbmi.hms.harvard.edu/)

Original data of both data sets is in xml format, but there is small difference of internal structure. I define xml2excel function separately.

## Goal
Target is to update the pretrained Spacy model using available, evaluate the performance with Precision, Recall and F1 score.

## Main steps
* Preprocess the data to meet the reauirement of spacy.  Example: `['I lives in Chicago.', {'entities' : [11, 18, 'GPE']}]`

* Group some entities which are defined using different type names but represent same things, like group CITY and COUNTRY into GPE.

* Test, Train splits the model and train the model.

* Evaluate the new model performance on train and test data sets.

* Visualization with new model.

## Conclusion
[Spacy](https://spacy.io/usage/training) provides covenient API to train the model with new API. The updated model achieves around 0.93 F1 score after 100 iterations.
It is suspicously overfitting at that time.
