# ML_Strategy-design_v2

Improvement compared with Version 1:

I added several more technical indicators, including Momentum, MACD, RSI and Percentage Price Oscillator to enrich the features of the learning model.
Also tried other model, i.e., random forest, to learn from our features and generate trading signals.
Extended the backtest results and enable our strategy hold different numbers of stocks.
Conducted large numbers of result visulizations and comparisons based on different performance metrics.

Summary:

Conclusion:

The added technical indicators worsen the performance of learning models, which indicates the effectiveness of the original features of R and V series proposed by myself in Version 1.
The random forest model generates worse performance, which manifests that, with limited number of features, the more complicated model is prone to overfitting, and logistic regression is simple but useful.
For the returns of different time horizons, the model can get the best prediction (with highest precision and recall scores) for the probability of obtaining a return over 0.5% by holding stocks for 10 days.
For the proposed strategy, the maximum holding stock number of 10 or 15 can get good performance over various metrics, including return, sharp ratio, max drawdown and so on. If the maximum holding stock number is smaller than 10, i.e., 1,3 and 5, the max drawdown will be dramatically degraded; and if the maximum holding stock number is larger than 15, i.e., 20,30 and 50, the return will be lowered while the max drawdown will not be improved.
Till now, the performance of the proposed strategy is good and can achieve a sharp ratio over 2, while the performance of max drawdown can be further improved.

Future Directions:

More effective features can be proposed to facilitate the learning of different models, such as some risk related features to improve the max drawdown performance.
More kinds of machine learning techniques can be tried, such as lightGBM, xgboost, svm, mlp, LSTM and so on, and more opimization of hyperparameters has to be taken into account with methods such as cross validation.
Consider and deal with more practical issues in the backtest process. As an example, stocks may not be traded due to suspension, limit up or limit down.
Consider to apply such a similar machine learning method to other stock markets, such as US and CH markets.
Machine learning methods with decision-making process such as reinforcement learning techniques can be further explored to design trading strategies.
