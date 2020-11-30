# Portfolio Analysis

For this project, I applied quantitative analysis using Python and Pandas to determine which portfolio performs best in areas such as volatility, returns, risk, and Sharpe ratios.  The data that we used for this project comes from the historical daily returns of several portfolios: some from a firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. Finally, a custom portfolio of stocks is created and its performance is compared to that of the other portfolios, as well as the larger market (S&P 500).

## Data Preparation

* Read in several csv files and converted the dates to a `DateTimeIndex`.
* Detected and removed null values.
* Removed dollar signs from the numeric values and converted the data types as needed.
* Converted the S&P 500 closing prices to daily returns.
* Joined all dataframes into a single DataFrame with columns for each portfolio's returns.








