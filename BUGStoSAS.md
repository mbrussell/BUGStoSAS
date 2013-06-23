BUGS to SAS
========================================================

Introduction
-------------------------
This serves as an attempt to document similar syntax used in BUGS and SAS. General categories are separated into (1) common statistical distributions, (2) establishing the Markov chain, (3) plotting MCMC results, and (4) working with the posterior samples.


Any additions, corrections and/or suggested improvements are encouraged and appreciated. Send an [email](mailto:russellm@umn.edu). 

1. Common statistical distributions
-------------------------
------

Number | Distibution | Type | BUGS |SAS
------------- | ------------- | ------------- | -------------
1.1  |Bernoulli              | Discrete    | `dbern(p)`          |`f1`
1.2  |Binomial               | Discrete    | `dbin(p,n)`         |`bin(n,p)`
1.3  |Negative binomial      | Discrete    | `dnegbin(p,r)`      |`negbin(n,p)`
1.4  |Poisson                | Discrete    | `dpois(m)`          |`poisson(m)`
1.5  |Beta                   | Continuous  | `dbeta(a,b)`        |`beta(a,b)`
1.6  |Cauchy                 | Continuous  | Available in BUGS?  |`cauchy(a,b)`
1.7  |Chi-Square             | Continuous  | `dchisqr(k)`        |`chisq(k)`
1.8  |Exponential            | Continuous  | `dexp(m)`           |`expon(scale = m)`
1.9  |Gamma                  | Continuous  | `dgamma(r,n)`       |`gamma(r,scale = n)`
1.10 |Lognormal              | Continuous  | `dlnorm(a,t)`       |`lognormal(a,var = t)`
1.11 |Normal                 | Continuous  | `dnorm(m,t)`        |`normal(m,var = t)`
1.12 |Student's-t            | Continuous  | `dt(m,t,k)`         |`t(m,var = t,k)`
1.13 |Weibull                | Continuous  | `dweib(v,m)`        |`weibull(m,c,s)`
1.14 |Uniform                | Continuous  | `dunif(a,b)`        |`uniform(a,b)`
------

2. Establishing the Markov chain
-------------------------

------

Number | Description | BUGS |SAS
------------- | ------------- | ------------- | -------------
2.1 |Generate 0.1 as a starting value       |`inits = 0.1`         |`initial = 0.1`
2.2 |Specify 10,000 iterations as burn-in   |`n.burnin = 10,000`   |`nbi = 10,000`
2.3 |Specify 100,000 MCMC iterations        |`n.iter = 100,000`    |`nmc = 100,000`
2.4 |Specify thinning parameter as 3        |`n.thin = 3`          |`thinning = 3` or `thin = 3`
------


3. Plotting the MCMC results
-------------------------

4. Working with the posterior samples.
-------------------------
