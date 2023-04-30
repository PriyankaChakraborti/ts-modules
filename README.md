
A python package for multi-variate time series forecasting with various base estimators such as lightgbm and scikit-learn 

 Leverages the benefit of using scikit-learn syntax and components to map a complex time series forecasting problems into a tabular supervised regression task.

## Overview

Provides 4 optimized forecasting techniques:

- **Recursive Forecasting** 

Lagged target features are combined with exogenous regressors (if provided) and lagged exogenous features (if specified). A scikit-learn compatible regressor is fitted on the whole merged data. The fitted estimator is called iteratively to predict multiple steps ahead.

- **Direct Forecasting** 

A scikit-learn compatible regressor is fitted on the lagged data for each time step to forecast.


- **Stacking Forecasting** 

Multiple recursive time series forecasters are fitted and combined on the final portion of the training data with a meta-learner.


- **Rectified Forecasting** 

Multiple recursive time series forecasters are fitted on different sliding window training bunches. Forecasts are adjusted and combined fitting a meta-learner for each forecasting step.