# Challenge-4


## Analyzing Portfolio Risk and Return

I am a quantitative analyst for a FinTech investing platform. This platform aims to offer clients a one-stop online investment solution for our retirement portfolios that’s both inexpensive and high quality. To keep the costs low, the firm uses algorithms to build each client's portfolio. The algorithms choose from various investment styles and options. 

I've been tasked with evaluating four new investment options for inclusion in the client portfolios. Legendary fund and hedge-fund managers run all four selections. (People sometimes refer to these managers as **whales**, because of the large amount of money that they manage). I’ll need to determine the fund with the most investment potential based on key risk-management metrics: the daily returns, standard deviations, Sharpe ratios, and betas.

---

## Technologies

This project leverages Pandas on Jupyter notebook

---

## Open Guide

Before running the application first open Jupyter lab in terminal:

```
  1. Activate dev environment by: "conda activate dev"
  2. Open Jupyter Notebook by: "Jupyter lab"
```


---

## Usage

To use the analysis simply clone the repository and run the **risk_return_analysis.ipynb** within the Jupyter Notebook.\
*Import the following libraries and dependencies:*

``` python
Import pandas as pd
from pathlib import Path
import numpy as np 
%matplotlib inline 
```

---

## Analyze the Performance 

1. To analyze the data, use the *plot* function to visualize the daily return of the four funds portfolio and the S&P 500.
2. Use *cumprod* function to calculate the cumulative returns for four funds portfolio and the S&P 500.
3. Use *plot* to visualize the cumulative return
![<cumulative return>](<Images/Cumulative return.png>)

**Base on the visualization, I noted that none of the four fund portfolios outperform the S&P 500 Index.**


---

## Analyze the Volatility
1. Use *plot.box* function to visualize the daily return for four funds portfolio and the S&P 500.
2. *drop* to create the daily return for only four funds portfolio. 

![<daily return 4 funds>](<Images/daily return 4 fund.png>)

**Base on the the plot, Berkshire Hathaway INC is most volatile and Tiger Global Management LLC is least volatile.**

---

## Analyze the Risk
1. To calculate the Standard Deviation for four funds portfolio and the S&P 500, use *std* function, and *sort_value* to sort from the smallest to largest. 
1. To calculate the Standard Deviation for four funds portfolio and the S&P 500, use the formula: *standard deviation x sqr root of 252* and *sort_value* to sort from the smallest to largest. 
2. Use 21-day rolling window to plot the rolling Standard Deviation for four funds portfolio and the S&P 500 
![<21 day rolling sp>](<Images/21 day rolling sd sp.png>)
3. And the 21-day rolling window for only four funds portfolio
![<21 day rolling funds>](<Images/21 day rolling funds.png>)

**Based on the rolling metrics, the risk of each portfolio increase at the same time that the risk of the S&P 500 increases, and BERKSHIRE HATHAWAY INC poses the most risk.**

---

## Analyze the Risk-Return Profile
1. Use *mean* function * 252 to calculate annualized return 
2. To calculate Sharp ratio, use the formula: *annualized_return / annualized_standard_deviation*
3. Visualize the Sharpe ratio by *bar plot*
![<sharpe ratio>](<Images/sharp ratio.png>)

**Based on the box plot, BERKSHIRE HATHAWAY INC  offers best risk-return profile, PAULSON & CO.INC offers the worst.**

---

## Diversify the Portfolio 
1. Use *var* function to calculate the variance of the S&P 500 by using *60-day* rolling window 
2. I picked **BERKSHIRE HATHAWAY INC** and **TIGER GLOBAL MANAGEMENT LLC** as two portfolios based on their sharpe ratio 
3. Calculate covariance, beta and average beta to analyze both portfolios
4. Plot each portfolio to see the 60-Day rolling beta
![<berkshire>](<Images/berkshire.png>)
![<tiger>](<Images/tiger.png>)

**Based on both plot, BERKSHIRE HATHAWAY INC seems more sensitive to the movements in the S&P 500 as it has higher average beta of 0.22. I would recommend for BERKSHIRE HATHAWAY INC because higher average beta indicates greater return, also BERKSHIRE HATHAWAY INC has the best sharp ratio.**


---

## Contributors

Feier Ou 

ffeierou1003@gmail.com 

---

## License

Feier Ou 
