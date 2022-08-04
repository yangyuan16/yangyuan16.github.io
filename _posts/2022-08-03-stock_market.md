---
layout: post 
title: Some tips for observing and studying stock market 
description: summary of some view points, questions, inspirations, ...   
tag: Quantitative Analysis
---

### Chinese stock market
>There are two types of shares in the mainland China stock market, A-shares and B-shares. A-shares are quoted
only in <font color=red>renminbi</font>, while B-shares are quoted in foreign currencies, such as the U.S. dollar, and are available to foreign
investors on a larger scale. Foreign investors may have difficulties accessing A-shares due to Chinese <font color=red>government
regulations</font>, and Chinese investors may have difficulties accessing B-shares, mainly for currency exchange reasons.
Some companies choose to <font color=red>list</font> their shares in both the A-share and B-share markets. 
>According to public information, the Wind database serves more than 90% of Chinese financial 
>institutions and 70% of <font color=red>Qualified Foreign Institutional
Investors (QFII)</font> operating in China.
>中国大陆股市有两种股票，A股和B股。A股仅以人民币报价，而B股则以外币报价，如美国，并向外国投资者提供更大规模的服务。
>由于中国政府的监管，外国投资者可能难以获得A股，而中国投资者可能无法获得B股，主要是因为货币兑换的原因。
>一些公司选择在A股和B股市场上市。
>根据公开信息，Wind数据库服务于90%以上的中国金融机构和70%在中国运营的合格外国机构投资者（QFII）。 


### For Asset pricing
>Against this background, we ask whether, in such a market, <font color=red> technical indicators from collectivistic investment behavior </font> 
>matter more for asset pricing than <font color=red>firm fundamentals</font>.
>
>Cite from: [Machine-Learning in the Chinese Stock Market](https://doi.org/10.1016/j.jfineco.2021.08.017).

### government
>Therefore, we examine whether return predictability and portfolio performance are compromised for SOEs 
>where government signaling plays such a prominent role.
>
>Given that China has been experiencing a highly dynamic development through a series of structural breaks, implementing various 
financial reforms, and expanding its capital markets' openness, we conjecture that highly 
fiexible methods are required to account for the Chinese market's specificity.
>
>Cite from: [Machine-Learning in the Chinese Stock Market](https://doi.org/10.1016/j.jfineco.2021.08.017).




### Machine Learning
> As out-of-sample R^2 has some limitations for model selection, 
> we analyze the models' <font color=red>conditional predictive ability</font> using a 
> statistical test recently developed in <font color=red>Li, Liao and Quaedvlieg (2020)</font>,
> which allows us to compare the performance of machine learning methods 
> in different macroeconomic environments. 
>(R^2 并不能作为衡量所有机器学习模型的一个普适的指标。Li, Liao, Quaedvlieg 发展出的
>方法能够评价机器学习在宏观经济环境中的表现！！！)   
>
> We follow the standard approach in the literature 
> for <font color=red>hyperparameters selection</font>, <font color=red>model estimation</font>, 
> and <font color=red> performance evaluation </font>. 
> See, e.g., [Gu et al. (2020b)](https://doi.org/10.1093/rfs/hhaa009) 
> and [De Nard et al. (2020)](https://doi.org/10.1002/for.2859).
>
> In particular, we divide our data into three disjoint time periods while
> maintaining the temporal ordering: 
> the <font color=red>training sample (2000-2008)</font>, the <font color=red>validation sample (2009-2011)</font>, and 
> the <font color=red>testing sample (2012-2020)</font>. 
> The <font color=red>validation sample</font> is used to for optimizing the hyperparameters of our models.
> The testing sample contains the next twelve months of data right after the validation sample. 
> Meanwhile, both the validation sample and the one-year testing period are <font color=red>kept rolling forward</font>
> to include the next twelve months.
>
> We use the training sample to estimate the model parameters subject to some
> pre-specified hyperparameters for a specific machine learning model 
> (我们使用训练样本来估计特定机器学习模型的模型参数，这些参数受一些预先指定的超参数的约束。)
>
>Cite from: [Machine-Learning in the Chinese Stock Market](https://doi.org/10.1016/j.jfineco.2021.08.017).

### Predictors Classification
> (1) related to market liquidity
>
> (2) related to fundamental factors like valuation ratios (pe, eps, ep, roe)
>
> (3) industry dummy variables. 
>
> (4) interaction terms between stock-level characteristics and the eleven macroeconomic predictors.
> Using the Kronecker product:
>![](http://yangyuan16.github.io//images/posts/Quantitative_analysis/kron_predictors.jpg)
>
>Cite from: [Machine-Learning in the Chinese Stock Market](https://doi.org/10.1016/j.jfineco.2021.08.017).

### Empirical analysis
> (1) We start by exploring our models' prediction performance via out-of-sample
> predictive <font color=red>R^2</font> and discuss <font color =red>predictability</font> 
> across different subsamples of our data.
>
> #### Out-of-sample predictability
> * As in [Gu et al. (2020b)](https://doi.org/10.1093/rfs/hhaa009).
