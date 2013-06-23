BUGS to SAS
========================================================

Introduction
-------------------------
This serves as an attempt to document similar syntax used in BUGS and SAS for performing Bayesian analyses. General categories are separated into (1) common statistical distributions, (2) establishing the Markov chain, (3) plotting MCMC results, and (4) working with the posterior samples.

Much of the BUGS code relies on the [R2WinBUGS](http://cran.r-project.org/web/packages/R2WinBUGS/index.html) and/or [BRugs](http://cran.r-project.org/web/packages/BRugs/index.html) packages in R.

Any additions, corrections, and/or suggested improvements are encouraged and appreciated. Send an [email](mailto:russellm@umn.edu). 

1. Common statistical distributions
-------------------------
------

Number | Distibution | Type | BUGS |SAS
------------- | ------------- | ------------- | ------------- | -------------
1.1  |Binomial               | Discrete    | `dbin(p,n)`         |`bin(n,p)`
1.2  |Negative binomial      | Discrete    | `dnegbin(p,r)`      |`negbin(n,p)`
1.3  |Poisson                | Discrete    | `dpois(m)`          |`poisson(m)`
1.4  |Beta                   | Continuous  | `dbeta(a,b)`        |`beta(a,b)`
1.5  |Cauchy                 | Continuous  | Available in BUGS?  |`cauchy(a,b)`
1.6  |Chi-Square             | Continuous  | `dchisqr(k)`        |`chisq(k)`
1.7  |Exponential            | Continuous  | `dexp(m)`           |`expon(scale = m)`
1.8  |Gamma                  | Continuous  | `dgamma(r,n)`       |`gamma(r,scale = n)`
1.9  |Lognormal              | Continuous  | `dlnorm(a,t)`       |`lognormal(a,var = t)`
1.10 |Normal                 | Continuous  | `dnorm(m,t)`        |`normal(m,var = t)`
1.11 |Student's-t            | Continuous  | `dt(m,t,k)`         |`t(m,var = t,k)`
1.12 |Weibull                | Continuous  | `dweib(v,m)`        |`weibull(m,c,s)`
1.13 |Uniform                | Continuous  | `dunif(a,b)`        |`uniform(a,b)`
------

2. Establishing the Markov chain
-------------------------

------

Number | Description | R2WinBUGS |SAS
------------- | ------------- | ------------- | -------------
2.1 |Generate 0.1 as a starting value       |`inits = 0.1`         |`initial = 0.1`
2.2 |Specify 10,000 iterations as burn-in   |`n.burnin = 10,000`   |`nbi = 10,000`
2.3 |Specify 100,000 MCMC iterations        |`n.iter = 100,000`    |`nmc = 100,000`
2.4 |Specify thinning parameter        |`n.thin = `          |`thin = ` or `nthin = `
2.5 |Specify the maximum number of tuning loops       |?    |`maxtune =`
2.6 |Specify the maximum number of tuning loops       |?    |`mintune =`
2.7 |Specify the number of tuning iterations       |?    |`ntu =`
------


3. Plotting the MCMC results
-------------------------

------

Number | Description | BRugs |SAS
------------- | ------------- | ------------- | -------------
3.1 |Trace plots       |`samplesHistory ('*')`         |`plots = trace`
3.2 |Posterior density plots   |`samplesDensity ('*')`   |`plots = density`
------

4. Working with the posterior samples
-------------------------
------

Number | Description | BUGS |SAS
------------- | ------------- | ------------- | -------------
4.1 |Data set named containing posterior samples of parameters      | Check coda         |`outpost =`

------
