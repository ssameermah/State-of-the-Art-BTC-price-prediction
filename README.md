# State-of-the-Art-BTC-price-prediction

### Introduction
Social media websites like Twitter are a medium for people to share their thoughts on the on-going events or past events. Twitter is believed to be a great source to understand what the general people are thinking about a certain topic and what is their sentiment with respect to that topic.

This abundnce of people sentiment can be harnessed to predict bitcoin prices. Generally people sentiment aligns with the market's behaviour and this is what we want to learn to make predicitons. Although, we have many other features that can be used to improve the results instead of just prediciting using tweets.

### Dataset
Our compiled dataset comes from various soucrces. The tweets data for 16M tweets was obtained from kaggle. Where as other features were scrapped from various websites like google trends, bitinfocharts.com, etc.

Here is the data description of the attributes used.

Bitcoin inflation rate: The percentage of new coins issued, divided by the current supply.
Mining Difficulty: The current estimated number of hashes required to mine a block.
Hash rate: The average estimated number of hashes per second produced by the miners in the network.
Transaction count: Bitcoin transactions per day.
Vol. : Trading Volume of bitcoin
Change %: % change since last day
Total tweets: No of tweets per day related to bitcoin
Google trends: Google search trend score for bitcoin
new_senti : Newly generated sentiment scores that are weighted using retweets, replies and sentiment scores.

### State of the Art Time Series forecasting models

**Temporal fusion transformer(TFT)**
This model supports mixed covariates (includes past covariates known for input_chunk_length points before prediction time and future covariates known for output_chunk_length after prediction time).

The TFT applies multi-head attention queries on future inputs from mandatory future_covariates. Specifying future encoders with add_encoders (read below) can automatically generate future covariates and allows to use the model without having to pass any future_covariates to fit() and predict().

By default, this model uses the QuantileRegression likelihood, which means that its forecasts are probabilistic; it is recommended to call :func`predict()` with num_samples >> 1 to get meaningful results.

**Temporal convolution network (TCN)**
TCN adds certain properties of recurrent neural networks to the classic CNN design.
The TCN ensures causal convolution. An output value must only depend on values that are positioned earlier in the input sequence.
Dilations in the TCN expand the receptive field of a node to encompass more historical periods.


**NBEATS**
N-BEATS is a state-of-the-art model that shows the potential of pure DL architectures in the context of the time-series forecasting. It outperforms well-established statistical approaches on the M3, and M4 competitions.

### Deep Learning Architectures Used
1. Fully Connected Dense Layer model
2. LSTM
3. CNNLSTM Architecture
4. Ensembling Models

