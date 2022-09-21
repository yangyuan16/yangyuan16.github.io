---
layout: post 
title:  Notes for reading papers related to Anomalies in Chinese Market. 
description:    
tag: Reading notes of financial studying
---

### Abstract
> Notes for reading papers 
> * [Finding Anomalies in China,
KeWen Hou, Fang Qiao, Xiaoyuan Zhang (2021)](http://cfrc.pbcsf.tsinghua.edu.cn/ueditor/php/upload/file/20210611/1623389943123279.pdf?l=en&y=2022?l=en&y=2021)  
> * [Replicating Anomalies in China,
Fang Qiao (2021)](https://www.cafr-sif.com/2019/2019selected/Replicating%20Anomalies%20in%20China.pdf).
> * [Anomalies in the China A-share market (2021)](https://doi.org/10.1016/j.pacfin.2021.101607) 
> * [Hus, Viswanathan, Wang, Wool (2017)]()
> * [Liu, Stambaugh and Yuan (2019)]()
> * [Carpenter, Lu, and Whitelaw (2018)]()
> * [Chen, Kim, Yao, and Yu (2010)]() 
> * [China A-shares, FAQs, facts, and figures](https://www.ubs.com/global/en/assetmanagement/insights/thematic-viewpoints/apac-and-emerging/articles/stock-connect-china-a-shares-faqs-equity-investing.html)

### Finding Anomalies in China, KeWen Hou, Fang Qiao, Xiaoyuan Zhang (2021)

#### 概述

> * the Chinese stock market differs from the U.S. stock market in two important
aspects: <font color=red>trading environment</font> 
and <font color=red>information environment</font>.

> * After risk adjustment, we find that 97 CAPM alphas are significant,
16 CH3 alphas are significant and 15 CH4 alphas are significant.

> * The CAPM alphas are very similar to the raw return, indicating that 
the market risk fails to explain these anomaly returns.

> * In contrast, with embedded size, value and turnover effects, the
CH3 and CH4 models are able to explain away a significant part of anomaly
raw returns, and thus we foucs our discussion on alphas using this model.

> * Among the 16 significant alphas relative to CH3 factors, 7 anomalies are 
constructed using liquidity-related information, and 4 are related to 
accounting-related information. 

> * Among the 15 significant alphas relative to the CH4 factors, 
half of anomalies are from trading-related information and half of them 
are from accounting-related information.

> * we consturct the composite anomalies with score, Fama-MacBeth regression, 
Lasso, and Random Forest by combining many signals. 
In total, we construct 10 composite anomalies with all characteristics in each 
category, sub-category, and in total. 

> * We find that the majority of the composite anomalies can pass the 
multiple hurdle of 2.85
After risk adjustment with the CH3 factors, almost half of the composite anomalies 
are still significant, with the majority of them from trading-related anomalies.

> * There are still signigicant CH4 alphas using random forecast method, which
are from the trading-related group. <font color=red> It indicates that the 
popular machine learning methods of Lasso and Random Forest outperform the 
traditional methods of score and Fama-MacBeth regression</font> 
The composite anomalies confirm that trading-related anomalies are 
very important in China.

> * We compare the anomaly results in China with those in the United States, as in Hou, Xue
and Zhang (2019), and identify three major differences. First, out of the 426 anomalies, 23% of
anomalies are significant in China, which is lower than the replication rate (35%) in the United
States, with the same hurdle being the absolute t-value above 1.96.

> * Second, most of the significant anomalies in China are trading-related anomalies, using
characteristics such as volatility, turnover, and dollar trading volume, especially liquidity
measures; while almost all trading frictions anomalies are insignificant in the United States as in
Hou, Xue and Zhang (2019). 

> * Third, most of the significant anomalies in the United States are driven by firm fundamental
information in accounting statements, such as value, investment, and profitability; while in China,
these variables mostly cannot provide statistically significant information about future stock
returns. 

> * All papers find that some anomalies working in the United States may mot
be replicated in other countries.

> * Jacobs and Muller (2019) study how 241 anomalies decay after publication 
across 39 international markets, and find that the United States is the only
country with a reliable post-publication decline in long-short returns.

> * A share: are the shares of chinese firms that listed on Shanghai and Shenzhen 
exchanges, and are open to domestic investors to trade. 

> * For the accounting information, the data on the balance sheet and income 
statement stat in 1990, and the data on the cash flow statement start from 
1997. Before 2002, financial statements are reported annually or semiannually,
and after 2002, they are reported quarterly. 

> * For the data on balance sheet, income statement and cash flow statements,
we fill in the missing quarterly data for calendar March and September with 
the most recent quarterly data.

> * We obtain the <cont color=red> analyst earnings forecasts data </font>
from Go-goal.com, which is the most comprehensive, accurate analysts's forecast
database, and widely used in fund industry in China.

> * quarterly institutional ownership: it reports the 
proportion of shares held by funds, brokers, insurance, security funds,
insurance companies, and trust companies etc.

#### Anomaly construction

> * We implement <font color=red> single portfolio analysis to test whether the anomalies can 
predict stock returns </font>.

> * For each anomaly, we follow the <font color=red>[k, m, n] approach as 
in Jegadeesh and Titman (1993) </font>.

> * Suppose the current month is t. We first 
collect <font color=red>firm-level information </font> 
to be used as anomaly sorting variables over [t-k+1, t].
(相当于财报采用ffill方式填充)

> * At time t, we sort A-share stocks into decile groups based on the 
sorting variables. Decile 1 contains the 10% of stocks with the lowest 
sorting variable values, while decile 10 contains the 10% of stocks with the 
largest sorting variable values. 

> * Then we wait a period of m months over [t, t+m]. 

> * if investors prefer immediate investment, we set m to be zero.

> * We hold the decile portfolios, determined at time t, over the next 
[t+m+1, t+m+n] months. 

> * The value-weighted decile portfolio raw returns are computed using 
previous month-end firm market capitalization as weights.

> * We also <font color=red>provide results using equal weights </font>.

> * If the anomaly sorting variable can predict future return, we expect to
see a significant difference in raw returns between decile 10 and decile 1,
over the holding period of [t+m+1, t+m+n]. 

> * The choice of the parameter k, m, n depends on the specific anomalies.

> * For instance, <font color=red>the waiting period m is zero except for 
momentum anomalies</font>, and the holding period n is generally 
set to be 1-, 6-, or 12-month.

> * The anomaly sorting variables, <font color=red>if coming from accounting information</font>,
might be constructed over the previous year or quarter, while if the sorting variables 
are from trading, they can be constructed over the previous month. 

> * The choice of k, m, n for each anomaly is clearly marked for each anomaly 
in online Appendix B. 

> * Since Chinese trading rules and accounting standards are different 
from the United States. <font color=red>we made several adjustments to the original 
sorting procedures by Hou, Xue and Zhang (2019) for the U.S. data.</font>

> *  For example, due to daily price limit of 10%, <font color=red>we use the average of the 
five highest daily returns in one month to construct the maximum daily return</font>,
rather than using one highest daily return in one month as in the original procedure.

> * We also exclude the stock in the portfolio if it is suspended with zero trading
volume during the portfolio sorting date. 

#### Multiple Tests

 
#### New words

> * anomaly pattern
> * information environment
> * 192 are trading-related and 234 are accounting-related
> * shell-value contamination
> * shorting ban
> * firm-level liquidity measures
> * risk-adjusted returns 
> * multiple test hurdle
> * return with dividends
> * free float A share
> * quarterly institutional ownership  
> * we merge the above data based on stock code, which is unique for each firm.
> * filters: we impose several filters on our datasets
> * including actively traded and delisted firms
> * spikes: The large spokes are likely dirven by excessive trading around large
movements in stock prices, especially during market boom periods 
> * market boom periods

### Replicating Anomalies in China, Fang Qiao (2021)

#### 概述

> * 

### Anomalies in the China A-share market (2021)

#### 概述

> * 
