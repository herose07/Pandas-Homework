# Portfolio Analysis

For this project, I applied quantitative analysis using Python and Pandas to determine which portfolio performs best in areas such as volatility, returns, risk, and Sharpe ratios.  The data that we used for this project comes from the historical daily returns of several portfolios: some from a firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. Finally, a custom portfolio of stocks is created and its performance is compared to that of the other portfolios, as well as the larger market (S&P 500).

## Data Preparation

* Read in several csv files and converted the dates to a `DateTimeIndex`.
* Detected and removed null values.
* Removed dollar signs from the numeric values and converted the data types as needed.
* Converted the S&P 500 closing prices to daily returns.
* Joined all dataframes into a single DataFrame with columns for each portfolio's returns.

## Quantitative Analysis

### Performance Analysis

* Calculated and plotted cumulative returns.



* Based on the plot, the portfolios that outperform the S&P 500 are Algo1 and Berkshire Hathaway

### Risk Analysis

* Created a box plot for each of the returns.
* Calculated the standard deviation for each portfolio.
  * These standard deviations tells us that the portfolios that are riskier than the S&P 500 are Berkshire Hathway and Tiger Global Management LLC
* Calculated the annualized standard deviation (252 trading days).

### Rolling Statistics

* Plotted the rolling standard deviation of the various portfolios along with the rolling standard deviation of the S&P 500 using a 21 day rolling window.
  * The plot shows that the risk increases for each of the portfolios at the same time risk increases in the S&P
* Constructed a correlation table for the algorithmic, whale, and S&P 500 returns.
  * The correlation tables shows that Algo 2 and the Soros fund returns most closely mimic the S&P

* Plotted a rolling beta between Berkshire Hathaway and S&P 500 returns.
  * The plot shows that Berkshire Hathaway is sensitive to movements in the S&P 500
  
* Calculated the exponentially weighted moving average with a 21 day half-life.

### Sharpe Ratios

Calculated and visualized the Sharpe ratios using a bar plot.
Based off the sharpe ratios, Algo 1 definitely outperforms the market and the whale portfolios.

## Custom Portfolio

* Created a custom portfolio called "Hero" which consisted of Amazon, Microsoft, and Netflix stocks.
* Performed the same analysis as above.

### Conclusions

* Hero portfolio is more volatile than the S & P 500
* According to the correlation analysis, Hero portfolio is most correlated with Berkshire Hathaway and the S & P 500, however, this is a rather weak correlation
* According to sharpe ratio analysis, Hero portfolio has a lower sharpe ratio than most of the other funds
* According standard deviation analysis, Hero portfolio demonstrates higher volatility than almost all other funds during the 21 day window
