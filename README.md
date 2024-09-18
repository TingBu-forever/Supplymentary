# Supplymentary
The details of data preparation for paper "Enhancing Multistep Prediction of Multivariate Market Indices Using Weighted Optical Reservoir Computing"

## Benchamarks
Benchmarks in this paper include seven global market indices that list in Table 1 below. 
![table 1](https://github.com/user-attachments/assets/0f2e285a-b8f6-415c-8d96-f4db600bf6ae)


## Feature selection
Due to the complexity of the benchmarks, a prediction model based solely on the closing price cannot gather all the necessary information for accurate predictions. Consequently, feature selection is a crucial part of the prediction enhancement. However, it is challenging to extract features from financial data. On the one hand, limiting the features can hinder the predictive model's performance. On the other hand, including all available features from the financial market can lead to a dimensionally complex and difficult-to-interpret model. Additionally, collinearity among multiple variables can negatively impact the model's performance. Therefore, we select seven main features either from macroeconomic indicators or technical indicators as the prediction inputs, as listed in Tabl 2. These features are chosen based on their high correlation with the closing price. As macroeconomic data can significantly impact the stock market, we consider the Cboe Volatility Index (VIX), the Interest Rate (EFFR), the Consumer Sentiment Index (UMCSENT), and the US Dollar Index (DXYNYB). The technical indicators include Moving Average Convergence Divergence (MACD), Average True Range (ATR), and Relative Strength Index (RSI). The details of the features are listed in Table 2. The correlation matrix among features is illustrated in the Fig.1 (b). These values are depicted based on the intensity of the color, indicating the strength of the relationship between the given variables. In the following RC prediction, we add the bottom row of the correlation weight (CW) matrix as extra input weights \(W_{cor}\). For each index, we used 500 days as the training data and 100 days as the testing data, as shown in Fig.1 (a). Each day, the training input is the previous day's closing price and the seven selected features. 

![table 2](https://github.com/user-attachments/assets/abac033e-5c7e-4855-99f9-a6cf9295c043)


<img width="800" alt="train_correlation" src="https://github.com/user-attachments/assets/3056b782-c05b-4d96-b179-5c9ff96514bc">

Fig.1.(a) An overview of one stock index sequence ^NYA with training and testing parts. (b) A feature correlation matrix heatmap for ^NYA


## References
[1] https://arxiv.org/abs/2408.00652

