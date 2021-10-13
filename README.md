# Stacking Machine Learning Models for Multivariate Time Series
Crafting an ensemble stack of machine learning models to use on the Beijing hourly PM 2.5 air pollution dataset (2015). The article showcases how machine learning methods may be used effectively on multivariate time series data. The stack ensemble included a diverse mix of linear models, tree-based models, support vector models and neural networks as base models. The final meta model was the all-time favourite OLS. The target variable was the one-hour ahead PM 2.5 air pollution level.

The data exhibited significant outliers and complex seasonalities, and was plagued by missing target values. After pre-modelling data analysis and engineering, the data was split three-ways, according to its temporal order, with the latest 10% of the data taken as the holdout test set. The remaining 90% of the data was in turn spliced into an earlier gridsearch training set (2/3) for the base models, and a later meta training set (1/3) for the meta model. The training data (previous 90%) was also used to run a 5-fold forward chain cross-validation procedure to assess model performance, for all the models used. The cross-validation found that the Stack Model generally outperformed the individual base models on MAE and RMSE scores.

The subsequent results on the holdout test set showed the Stack Model with the best MAE and RMSE scores. The stack's scores also evinced a 5–6% improvement over the baseline Persistence Model. In conclusion, the exercise demonstrated the effectiveness of a machine learning ensemble stack approach to multivariate time series data.
