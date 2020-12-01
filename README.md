![image](https://user-images.githubusercontent.com/65314799/100803849-7ea7e780-33f1-11eb-873e-a8065d125b07.png)

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

![image](https://user-images.githubusercontent.com/65314799/100804076-d7778000-33f1-11eb-9514-f08d3f05d504.png)

* Based on the plot, the portfolios that outperform the S&P 500 are Algo1 and Berkshire Hathaway

### Risk Analysis

* Created a box plot for each of the returns.

![image](https://user-images.githubusercontent.com/65314799/100803959-a6974b00-33f1-11eb-86d3-a64747b3ef49.png)

* Calculated the standard deviation for each portfolio.
  * These standard deviations tells us that the portfolios that are riskier than the S&P 500 are Berkshire Hathway and Tiger Global Management LLC
  
  ![image](https://user-images.githubusercontent.com/65314799/100804134-f0803100-33f1-11eb-9a3c-1314873e364f.png)

* Calculated the annualized standard deviation (252 trading days).

![image](https://user-images.githubusercontent.com/65314799/100803897-90898a80-33f1-11eb-8ce9-fbd24eb02db2.png)

### Rolling Statistics

* Plotted the rolling standard deviation of the various portfolios along with the rolling standard deviation of the S&P 500 using a 21 day rolling window.
  * The plot shows that the risk increases for each of the portfolios at the same time risk increases in the S&P
 
  ![image](https://user-images.githubusercontent.com/65314799/100804485-916eec00-33f2-11eb-87cb-30c141301d7a.png)

  ![image](https://user-images.githubusercontent.com/65314799/100804336-4f45aa80-33f2-11eb-9557-b7abfc41e0a3.png)

* Constructed a correlation table for the algorithmic, whale, and S&P 500 returns.
  * The correlation tables shows that Algo 2 and the Soros fund returns most closely mimic the S&P

![image](https://user-images.githubusercontent.com/65314799/100804014-badb4800-33f1-11eb-98dc-61927514e57e.png)

* Plotted a rolling beta between Berkshire Hathaway and S&P 500 returns.
  * The plot shows that Berkshire Hathaway is sensitive to movements in the S&P 500
  
  ![image](https://user-images.githubusercontent.com/65314799/100804421-77cda480-33f2-11eb-83d6-5c1780d1d314.png)

* Calculated the exponentially weighted moving average with a 21 day half-life.

![image](https://user-images.githubusercontent.com/65314799/100804386-64bad480-33f2-11eb-987e-4d166b927455.png)


### Sharpe Ratios

Calculated and visualized the Sharpe ratios using a bar plot.
Based off the sharpe ratios, Algo 1 definitely outperforms the market and the whale portfolios.

![image](https://user-images.githubusercontent.com/65314799/100804548-b3686e80-33f2-11eb-9280-f87cf4732dde.png)

## Custom Portfolio

* Created a custom portfolio called "Hero" which consisted of Amazon, Microsoft, and Netflix stocks.
* Performed the same analysis as above.

![image](https://user-images.githubusercontent.com/65314799/100804213-1ad1ee80-33f2-11eb-9c0a-5b994448c33c.png)

![image](https://user-images.githubusercontent.com/65314799/100804169-05f55b00-33f2-11eb-98e5-3b11a401f11a.png)

![image](https://user-images.githubusercontent.com/65314799/100804267-2f15eb80-33f2-11eb-98d0-af253fb12451.png)

![image](https://user-images.githubusercontent.com/65314799/100804303-41902500-33f2-11eb-9a2e-e59014e2a691.png)

### Conclusions

* Hero portfolio is more volatile than the S & P 500
* According to the correlation analysis, Hero portfolio is most correlated with Berkshire Hathaway and the S & P 500, however, this is a rather weak correlation
* According to sharpe ratio analysis, Hero portfolio has a lower sharpe ratio than most of the other funds
* According standard deviation analysis, Hero portfolio demonstrates higher volatility than almost all other funds during the 21 day window
