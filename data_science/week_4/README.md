# DATA SCIENCE CHALLENGE SCL WEEK 4 - Predicting card fraud

# BACKGROUND

The datasets contains transactions made by credit cards in September 2013 by european cardholders. It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, ... V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise. 
The dataset has been collected and analysed during a research collaboration of Worldline and the Machine Learning Group (mlg.ulb.ac.be) of ULB (Université Libre de Bruxelles) on big data mining and fraud detection.

# TASK

Create a predictive algorithm (Machine Learning, NOT ANN) to predict if a transaction is fraud (class 1) or not (class 2)
--- 
# DATASETS

Columns:
   * 0 -> Time, numeric variable
   * 1-28 -> Predictive numeric features
   * 29 -> Amount, numeric variable 
   * 30 -> Class, this is the target. It is a nominal variable with just 2 unique values (0 and 1)
---
# DELIVERY

Paste the link to your Github repository with two files, one containing all the code you have made in either '.py' or '.ipynb' format. And another file with the values predicted by your algorithm. The file with the predictions has to be a '.csv' and only has to be a column with the predictions as it appears in the example file 'example_predictions_delivery.csv'.
