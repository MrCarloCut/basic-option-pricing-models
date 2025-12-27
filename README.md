# basic-option-pricing-models

Black–Scholes, Monte Carlo with confidence intervals, and CRR binomial trees  
(European and American options)

> Mathematics MSc project

---

## Project Overview

For European call and put options, the closed-form Black–Scholes price is used as the reference (true) value.

The aim of this project is to analyze the **accuracy–time trade-off** of the Cox–Ross–Rubinstein (CRR) binomial model and Monte Carlo (MC) simulation for at-the-money European options.

Monte Carlo estimators produce random prices and random confidence intervals.  
To account for this variability, results are **averaged over multiple independent runs**.

For Monte Carlo simulations, prices, confidence interval widths, and execution times are reported for different numbers of simulated paths:
- 100  
- 1,000  
- 10,000  
- 100,000  

The CRR method is deterministic; therefore, its performance is evaluated in terms of **pricing error** and **execution time** as the number of time steps increases.

Finally, the CRR binomial tree is applied to **American call and put options**, highlighting the role of early exercise.
