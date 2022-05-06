# Unit 10—A Yen for the Future

![Yen Photo](Images/unit-10-readme-photo.png)

## Background

The financial departments of large companies often have to make foreign currency transactions when doing international business, while hedge funds are also interested in anything that will provide an edge in predicting currency movements. Hence, both are always eager to gain a better understanding of the future direction and risk of various currencies. 

- - -

### SUMMARY

#### Time-Series Forecasting


1. Plotting the Settle price to check for long or short-term patterns.

![pattern](Images/trend.png)
   
    * Do you see any patterns, long-term and/or short?

Over 20 years, it is clearly that CAD is weakened over JPY since its peak of 137.28. Looking back 10 years, CAD/JPY is trading in a range between 70 and 100. However in short-term, since begining 2020 CAD is trading under 200 days of moving average showing a negative momentum. However, looking at the chart, in short term the price is hard to break the all-time low

2. Decomposition using a Hodrick-Prescott filter (decompose the settle price into trend and noise).

![trend](Images/price_vs_trend.png)

![noise](Images/noise.png)


     *  Do you see any patterns, long-term and/or short?
* In short term, the trend show CAD/JPY recovers from its trough since 2015.

3. Forecasting returns using an ARMA model.
![ARMA](Images/ARMA.png)  
    
    * Based on the p-value, is the model a good fit?
* p_value of Lag 2 = 0.14 which is higher than 0.05 -> the model is not a good fit at all.
4. Forecasting the exchange rate price using an ARIMA model.
![ARIMA](Images/ARIMA.png)  
    
    * What does the model forecast will happen to the Japanese Yen in the near term?
 * According to ARIMA model, the CAD/JPY decreases meaning that CAD continues to decrease and Japanese Yen is appreciated.

5. Forecasting volatility with GARCH.
![GARCH](Images/GARCH.png)
   
    * What does the model forecast will happen to volatility in the near term?
Volatility will increase in next 5 days. For companies dealing with a lot of fx transactions, they may think of hedging the risk. For hedge fund, it's time for arbitrage.

Use the results of the completed time series analysis and modelling to answer the following questions:

1. Based on your time series analysis, would you buy the yen now?

Not yet enough information for me to buy yen now. ARMA and ARIMA both are not qualified to pass 95% confidence interval. While GARCH shows the increase of volatility but up or down side I am not sure yet.


2. Is the risk of the yen expected to increase or decrease?
According to GARCH model, the risk is expected to increase

3. Based on the model evaluation, would you feel confident in using these models for trading?

I do not depend solely on these models. For ARMA and ARIMA with 95% confidence interval, high p-value makes model insignificant. GARCH seems to be better among all, but its BIC and AIC are both higher than ARIMA. 

After all, when thinking about using the models trading, I surely need more information, also need time to validate and test the model to decide whether or not to use it.

---

© 2021 Trilogy Education Services
