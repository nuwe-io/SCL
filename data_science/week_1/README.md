# DATA SCIENCE CHALLENGE SCL WEEK 1 - Predicting Cardano price movements

# BACKGROUND

[Cardano](https://cardano.org/) is one of the most important cryptocurrencies in the [cryptocurrency market](https://coinmarketcap.com/), and it is also one of the most volatile in the top 10. Currently the cryptocurrency market is a highly speculative market in which there are large players who are making large profits through the use of bots that buy and sell when they detect anomalous movements, and who benefit from the high volatility in prices, the more volatility there is, the higher the profit margins obtained. As this is a market in which the majority of large movements are made by bots, it is not unreasonable to think that bots can be used with just a few pieces of market data to detect price trigger actions and take advantage of them.


---
# TASK

Create a predictive algorithm (Machine Learning or Deep Learning) to predict the correct time to buy cardano and the correct time to sell, these are defined by the 'target' column of the 'train.csv' dataset. Once the predictive algorithm is done, it has to be used with the testing predictors dataset. 

--- 
# DATASETS

For this challenge two [datasets](https://github.com/nuwe-io/SCL/tree/main/data_science/week_1) are provided, the dataset for training the predictive algorithm and the dataset for testing the predictive algorithm.

Each row of the dataset represents features of the trades done in periods of 5 minutes. The train + test dataset contains information of the pair ADA/USDT of 63 days.

## train.csv
*Shape (12701 rows, 11 columns)*

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

* **Volume** -> Amount of cryptocurrecies transactionated in the 5 minutes timeframe
* **QV** -> Quote asset Volume, amount of USD transactionated in the 5 minutes timeframe
* **NOT** -> Number Of Trades, this mean the total number of transactions done in the 5 minutes timeframe
* **TBB** -> (Taker Buy Base) Amount of crypto bought directly with a market order
* **TBQ** -> (Taker Buy Quote) Amount of USDT bought directly with a maket order
* **Volatility** -> Is the relative change between the close price and the open price of each timeframe [%] 


### Target
Column 11 -> target to predict 

This column shows 3 values that goes from 0 to 2. Where each of these values corresponds to one order. These orders can be later be executed by a bot

| Value | Order |
|:-----:|:-----:|
|   0   |  Wait |
|   1   |  Buy  |
|   2   |  Sell |


## test_predictors.csv
*Shape (5443 rows, 10 columns)*

Contains the same predictors as in the train set to test the accuracy of your predictive algorithm

---
# DELIVERY

Paste the link to your Github repository with two files, one containing all the code you have made in either '.py' or '.ipynb' format. And another file with the values predicted by your algorithm, the values that are 0,1 or 2. The file with the predictions has to be a '.csv' and only has to be a column with the predictions as it appears in the example file 'example_predictions_delivery.csv'.
