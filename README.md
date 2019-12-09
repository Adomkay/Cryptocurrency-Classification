# Cryptocurrency-Classification
Cryptocurrency classification
This is a project to classify criptocurrencies based on historical ticker data. The dataset contains input information on 'Open', 'Low', 'High', 'Close', 'Trades' and 'Volume'. It also contains classification output information 'Y' (0,1). The objective is to model an algorithm that can accurately classify the output based on the input

# Methodology
I used 2 broad approaches: Supervised learning and Deep Learning. 

For the supervised learning approach first transformed the time series data into a format that could then be used for supervised machine learning. The first way I went about this was to create a time window with memory. This means that I transformed the timeseries into a dataset that had all input information from time t-n to t-1 (where t is current time and n is the time window size) as input features and the classification output at time t as the corresponding dependent variable. I then applied the supervised machine learning algorithms to the transformed dataset

The second way I approached the time series transformation using time window was to simply shift the target variable downwards in time by the size of the time window (n). I then applied the supervised machine learning algorithms to the transformed dataset.

For the deep learning approach I used a vanilla ANN and LSTM. I transformed the time series data into the input format that LSTM requires before fitting the model on the data.
