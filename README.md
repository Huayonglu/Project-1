# Project-1 12-Month Momentum Investment Strategy

## Background

Beating the market has always been the final and sole goal of every investor who takes an active approach to investing, rather than following the stock market index tracking indices (passive). In this project, we try to pursue our investment strategy on cross-sectional momentum, to create a superior, robust and outperforming portfolio. We use a mix of libraries, packages and API to provide us the most suitable data as well as organize the findings in a sophisticated and presentable method.    

#### Rationale
The momentum premium (the amount momentum strategies work over the market) is well documenated in academia, and we look to test that on our universe of approximately 2500 NYSE listed stocks. One important feature of quantitative investment strategies is the economic rationale behind why it works (if it does), as otherwise people can be critical of potential data-mining or a 'black-box' approach with no intuition. The momentum factor generally is one that falls into the bucket of a 'behavioural anomly', as intuitively one can deduct that there is probably information in the trends of moving prices or fundamentals. For example, one of the most common behavioural reasonings is "investor herding", where investors tend to overreact to a trend and get overconfident about a particular asset, driving prices up even further than they should be (and vice versa with underreaction in selling a stock). 


## Base Strategy 

1. Collect the closing prices of active stock in NYSE that can be dated back to 2002
2. Clean up dataframe e.g. remove nulls and transform the index - ultimately reduce the data in dataframe
3. Calculate annual return from each stock ticker
4. Sort the values and find the top 100 best performing from each month 
5. Build and reconstruct the monthly portfolio from the sorted data, then substract it by 0.5% of the monthly return as transactional cost 
6. Similar to procedure above, grab the 12-month return of a comparable **benchmark** from 2002, which in our case we use S&P 500 or 500 largest trading US companies
7. Compare and visualize both investment returns
8. Backtest the strategy with different variables


## Technology Used
1. alpaca API (gathering ticker)
2. yahoo Finance (collecting prices from each ticker)
3. pandas
4. numpy
5. request
6. quandl 
7. math
8. hvplot
9. datetime
10. os
11. quantstats (visualization of findings)
12. sklearn.linear_model (regression analysis)
13. statsmodel (regression analysis)

## Screeshots of Findings

-  **Key Stats**

![Stat](Stats.png)

Though the strategy witnessed strong volatility, the the risk-adjusted return (sharpe) of this strategy immensely outperformed the S&P 500 and almost yields twice as much returns on a cumulative basis over ~20 years.

- **Performance Cumulative Returns**

![Performance Cumulative Returns](Performance_Cumulative_Returns.png)


- **Comparison Distribution of Returns** 

![Distribution](Distribution%20.png)

As can be seen, our strategy is more volatile than S&P 500. There are moments where our return could draw down by 20% and jump in similar magnitude, while S&P 500 max monthly drop and increase is only  10%

- **Distribution with SNS**

![Distribution with SNS](Distribution_with_SNS.png)

- **Max Drawdown** 

![Max Drawdown](Max_Drawdown.png)
Two major drawdown occured during 2008 and 2020 where global financial crisis and COVID-19 pandemic took place.

- **Rolling Beta**

![Rolling Beta](Rolling_beta.png)

- **Rolling Volatility**

![Rolling Volatility](Rolling_Volatility.png)

Similar to other indication, our strategy pose extra risk and may not suitable for risk-averse investor

- **What happens when you change some parameters in the model? - Sharpe Ratio**

![Sharpe Ratio](Sharpe_Ratio.png)

This graph illustrates the outcome of how different a variety of lookbacks, as well as concentration levels, can influence the returns. Taking a greater concentration in stocks reduces diversification but may increase your risk-adjusted return. In our case, it seems that 6 or 12 months is the best, but the added diversification that 100 stocks gives seems to be the better bet as there isn't a huge benefit for concentrating the portfolio more. Also, it's best for us to stick with 12 months lookback, as it provides the more robust results.


- **All Monthly Returns**

![All Monthly Returns](All_Monthly_Returns.png)

We have most months with positive returns, with a few major drawdowns during recessioniary environments.

## Member
- Abigail
- Albertyo
- John
- Luis

