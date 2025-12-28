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

## Monte Carlo Method results

The fixed parameters are: S0=100, T=5, k=100, sigma=0.3, r=0.05.\
The reference value is computed using the black_scholes_formula() function and it is 35.9578. 

| N        | MC estimate | Interval width | Error  | Avg execution time (s) |
|----------|-------------|----------------|--------|------------------------|
| 100      | 35.6343     | 25.248         | 0.3235 | 0.000558               |
| 1,000    | 35.7803     | 8.0673         | 0.1775 | 0.000728               |
| 10,000   | 36.0352     | 2.6017         | 0.0774 | 0.001108               |
| 100,000  | 35.9390     | 0.817          | 0.0188 | 0.004642               |

As expected from theory, the Monte Carlo estimator converges at a rate of 1/√N.  
This behavior is empirically confirmed by the decreasing errors and confidence interval widths as N increases.  
On the other hand, the computational cost grows linearly with the number of simulations, in agreement with the theoretical complexity of the method.
