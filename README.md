# Time_Series_ARIMA
This was a small passion project involving stock market predictions using an ARIMA model.


## Overview

This data is stock market information spanning from 2006 to 2019 across over 30 companies.  The data was taken from Kaggle which can be found [here](https://www.kaggle.com/camnugent/sandp500?select=all_stocks_5yr.csv).  Out of all the companies the final anlysis was focused on google.  I wanted to try to simplify this as much as possible since it was my first time working with time series. 



## Stationarity

Stationarity in our model tells us how predictable or reliable it will be.  Testing for stationarity was a common first step that I found everywhere when I started researching time series.  **Stochasticity** is the measurement of *how much* stationarity a time series has.  It is a variable or process that has uncertainty in it.  A stationary time series makes predictiions pretty straight forward where as a stochastic time series makes outcomes harder to predict.

Below are the rolling means and standard deviations of Google and Amazon Closing prices in the US Stock Market.

![rolling](photos/photo1.png)


## AD Fuller Test

We test for stationarity to confirm the suspicions with and Augmented Dickey Fuller Test.  ADF is a form of hypothesis testing used to test for the presence of what is known as a uit root.  The unit root or a unit root process is a stochastic trend in time series. The presence of this unit root implies unpredictability.

The hypotheses of these tests are:

*𝐻0: "Process has unit root".*

*𝐻a: "Process has NO unit root".*

The test statistic is: **1.322424**. 
Now you need to compare this with the critical values under 𝐻0.

The Critical Values are given with:

1%:−3.433 | 5%:−2.863 | 10%:−2.567

Since your test statistic is higher than all of the critical values you fail to reject 𝐻0 at a significance level > 0.05 and reject 𝐻a. You can conclude that your time series has a unit root, or unit root process. Statistically speaking, your process is not stationary. So, you fail to reject 𝐻0.

![ADF](photos/photo2.png)


## Differencing

Differencing is a method that can be used to remove stochasticity.
When differencing this data, I was able to acheive a perfectly straight line, that for all intensive purposes could be a rolling mean.



## Model



An Arima Model was used for this time series.


## Predictions





## Issues


I had a lot of issues with the syntax for getting predictions and plots of predictions.  This is something that required a lot of extra reading and understanding what I was doing wrong witht the model.  Syntactical issues continue to exist with modeling and predictions that are more user error than the programming language itself.  **WORK IN PROGRESS**


## Conclusion

