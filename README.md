# curiosity
Inquiries into statistics, economics, econometrics, python and data science

# [Exploring bias in default commands for variance, covariance and correlation in Numpy and Pandas](https://github.com/ivanadr/curiosity/blob/main/Biased%20unbiased.ipynb) 
* 📓 [Biased unbiased.ipynb](https://github.com/ivanadr/curiosity/blob/main/Biased%20unbiased.ipynb) 

**Motivation**   
Inquiry into implementation of bias into python functions calculating variance, covariance and correlation.   
**Learning outcome**     
Knowing what method python libraries use to calcualte variances so we can taylor their use to our need.  

**Conclusions** 
* numpy vs pandas (df, describe)
  * `np.var` and `df.var` have different defaults (the former is biased by default, the latter is unbiased by default)
  * either command can be adjusted to meet our needs with the `ddof` argument
* cov
  * is the same in both `np.cov()` and `df.cov()` as both are dividing by n-1 by default
  * the default setting within numpy: for `np.var` and `np.cov` differ (the former is biased by default, the latter is unbiased by default)
* corr
  * Bias does not matter for correlation:
  * we arrive at the same number as long as both covariance and variance are of the same kind (i.e. both biased or both unbiased)
