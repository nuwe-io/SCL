# DATA SCIENCE CHALLENGE SCL WEEK 2 - Predicting particles velocity

# BACKGROUND

NASA has designed a new type of sensor that, from measuring the electromagnetic variation in a field, it can estimate the velocity of one particle relative to the velocity of the other particle. In this challenge, the data obtained from this sensor will be used to train a predictive model to predict that relative velocity.
---
# TASK

Create a predictive MACHINE LEARNING (not ANN) algorithm to predict the relative velocity of the particles. The aim is to find the algorithm that minimizes the mean squared error (MSE).

--- 
# DATASETS

For this challenge two [datasets](https://github.com/nuwe-io/SCL/tree/main/data_science/week_2) are provided, the dataset for training the predictive algorithm and the dataset for testing the predictive algorithm.

### train.csv

(6 columns x 7000 rows) the first 5 columns contains the predictive variables and the 6 column contains the target to predict.

### X_test.csv

(5 columns x 3000 rows) contains the predictive variables to test your algorithm.

---
# DELIVERY

Paste the link to your Github repository with two files, one containing all the code you have made in either '.py' or '.ipynb' format. And another file with the values predicted by your algorithm. The file with the predictions has to be a '.csv' and only has to be a column with the predictions as it appears in the example file 'example_predictions_delivery.csv'.
