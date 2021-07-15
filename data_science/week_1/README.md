## DATA SCIENCE CHALLENGE SCL WEEK 1 

For this challenge two datasets are provided, the dataset for training the predictive algorithm and the dataset for testing the predictive algorithm.

Each row of the dataset represents features of the trades done in periods of 5 minutes. The train + test dataset contains information of the pair ADA/USDT of 63 days.

# train.csv
Shape (12701 rows, 11 columns)

| Open_time           | Open   | High   | Low    | Close  | Volume     | QV           | NOT  | TBB        | TBQ          | Volatility | target |
|---------------------|--------|--------|--------|--------|------------|--------------|------|------------|--------------|------------|--------|
| 2021-05-13 09:00:00 | 1.6625 | 1.6800 | 1.6623 | 1.6737 | 2878032.99 | 4.821304e+06 | 5125 | 1702161.28 | 2.851617e+06 | 0.673684   | 0      |

### Predictors
First 10 columns

* **Open_time** -> Time in which the candle starts. ('%Y-%m-%d %H:%M:%S')
* **Open** -> Open price of the candle, (price of the asset at the beggining of the 5 minutes)
* **High** -> Higher price of the asset in the 5 minutes period
* **Low** -> Lower price of the asset in the 5 minutes period
* **Close** -> Close price of the candle (price of the asset at the end of the 5 minutes)

![](https://github.com/nuwe-io/SCL/blob/main/data_science/week_1/images/candle.png)

* **Volume** -> 
* **QV** -
* **NOT**
* **TBB**
* **TBQ**
* **Volatility** -> Is the relative change between the close price and the open price of each timeframe


### Target
Column 11 -> target to predict 

This column shows 3 values that goes from 0 to 2. Where each of these values corresponds to one order. These orders can be later be executed by a bot.

| Value | Order |
|:-----:|:-----:|
|   0   |  Wait |
|   1   |  Buy  |
|   2   |  Sell |


# test_predictors.csv
Shape (5443 rows, 10 columns)

Contains the same predictors as in the train set to test the accuracy of your predictive algorithm.
