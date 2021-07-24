# Portfolio Management

Evaluating four new investment options for inclusion in client portfolios. This program helps determine the fund with the most investment potential based on key risk-management metrics: the daily returns, standard deviations, Sharpe ratios, and betas.

---

## Technologies

This project leverages python 3.7 with the following:

* [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/) - JupyterLab is a web-based user interface designed for data analysis.

* [pandas](https://github.com/pandas-dev/pandas) - Flexible and powerful data analysis / manipulation library for Python.

* [numpy](https://github.com/numpy/numpy) - The fundamental package for scientific computing with Python.

* [matplotlib inline](https://github.com/matplotlib/matplotlib) - Comprehensive library for creating static, animated, and interactive visualizations in Python.

---

### Installation Guide

Before running the application first install the following dependencies.

```python
  pip install jupyterlab
  pip install pandas
  pip install numpy
  pip install matplotlib
```

---

## Examples

**Creating daily returns DataFrame based on NAV prices of the Four Portfolios and on closing price of the S&P 500.**
```
daily_returns = whales_df.pct_change().dropna()
daily_returns.head()

```
**Visualizing the daily returns data of the Four Fund Portfolios and the S&P 500 using Pandas plot function.**
```
daily_returns.plot(figsize=(10,7), title="Daily Returns")

```

**Calculating, creating, and displaying the last five rows of cumulative returns DataFrame for the Four Fund Portfolios and the S&P 500.**
```
cumulative_returns = (1 + daily_returns).cumprod()
cumulative_returns.tail()
```

**Visualizing the cumulative return data of the Four Fund Portfolios and the S&P 500 using Pandas plot function.**
```
cumulative_returns.plot(figsize=(10,5), title="Cumulative Returns of Funds and S&P 500: 2014-2020")

```

**Visualizing the daily return data of the Four Fund Portfolios and the S&P 500 using Pandas plot function and box plot parameter.**
```
daily_returns.plot.box(figsize=(15,20), title="Daily Returns of Funds and S&P 500")

```

**Calculating standard deviation of the Four Fund Portfolios and the S&P 500; sorted from smallest to largest.**
```
standard_deviation = daily_returns.std().sort_values()
standard_deviation
```

**Calculating annualized standard deviation of the Four Fund Portfolios and the S&P 500; sorted from smallest to largest.**
```
year_trading_days = 252
annualized_standard_deviation = standard_deviation * np.sqrt(year_trading_days)
annualized_standard_deviation.sort_values()

```

**Visualizing the 21-Day Rolling Average of the Four Fund Portfolios and the S&P 500.**
```
daily_returns.rolling(window=21).mean().plot(figsize=(15,10), title="21-Day Rolling Average of Funds and S&P 500")

```

**Calculating the Sharpe Ratio of the Four Fund Portfolios and the S&P 500.**
```
sharpe_ratios = average_annual_return / annualized_standard_deviation
sharpe_ratios.sort_values()

```

**Visualizing the Sharpe Ratios of the Four Fund Portfolios and the S&P 500 in a bar chart.**
```
sharpe_ratios.plot.bar(figsize=(10,8),title="Sharpe Ratios")

```

**....**
```
profit_per_trade_early.plot(figsize=(10, 7), title="Profit Per Trade - Early Date", color="green")

```

**....**
```
profit_per_trade_early.plot(figsize=(10, 7), title="Profit Per Trade - Early Date", color="green")

```

**....**
```
profit_per_trade_early.plot(figsize=(10, 7), title="Profit Per Trade - Early Date", color="green")

```
---