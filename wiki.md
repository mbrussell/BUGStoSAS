BUGS to SAS
========================================================

Introduction
-------------------------
This serves as an attempt to document similar syntax used in BUGS and SAS. General categories are separated into (1) statistical distributions, (2) establishing the Markov chain, (3) plotting MCMC results, and (4) working with the posterior samples.


Any corrections or suggested improvements are encouraged and appreciated. Feel free to contribute to this wiki. Otherwise, send an [email](mailto:russellm@umn.edu). 

1. Statistical distributions
-------------------------

2. Establishing the Markov chain
-------------------------

| Number | Description | BUGS | SAS
--- | --- | ---
*Still* | `renders` | **nicely** | `niceeee`
3.1 | Generate 0.1 as a starting value | `inits = 0.1` | `initial = 0.1`
3.2 | Specify 10,000 iterations as burn-in | `n.burnin = 10,000` | `nbi = 10,000`

--------------------------------------------------
| No | Sadly        | There is none              |
--------------------------------------------------
| Except this, which is a poor alternative       |
--------------------------------------------------
| There really      | should be one              |
--------------------------------------------------

3. Plotting the MCMC results
-------------------------

4. Working with the posterior samples.
-------------------------