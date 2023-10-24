# Probability & Statistics
- [Probability and Statistics Cookbook](http://statistics.zone/)
- [STAT 415: Introduction to Mathematical Statistics](https://online.stat.psu.edu/stat415/)

## Bayesian statistics
- [Bayes' rule: Guide](https://arbital.com/p/bayes_rule/?l=1zq): intuitive guide to Bayesian reasoning
- 

### Bayesian sampling
- ["Importance sampling", Book Chapter by Art Owen](https://statweb.stanford.edu/~owen/mc/Ch-var-is.pdf)
- ["MCMC and Bayesian Modeling", by Martin Haugh @ Columbia University](http://www.columbia.edu/~mh2078/MachineLearningORFE/MCMC_Bayes.pdf): introduction to Bayesian modeling and MCMC sampling algorithms (Metropolis-Hastings and Gibbs Sampling)
- ["Information Theory, Inference, and Learning Algorithms", book by David J.C. MacKay](https://www.inference.org.uk/itprnn/book.pdf)
  - Chapter 29, "Monte Carlo Methods": uniform sampling, importance sampling, rejection sampling, the Metropolis method, Gibbs sampling, and slice sampling.
  - Chapter 37: "Bayesian Inference and Sampling Theory": criticism of the sampling theory (frequentist) approach vs the Bayesian approach
- ["Bayesian Data Analysis", book by Andrew Gelman, John Carlin, Hal Stern, Donald Rubin, David Dunson and Aki Vehtari](http://www.stat.columbia.edu/~gelman/book/BDA3.pdf)
  - Part III: Complete review of different sampling methods

## Statistical testing
- Two main approaches: https://en.m.wikibooks.org/wiki/Statistics/Testing_Data/Purpose
- Differences: [P Value and the Theory of Hypothesis Testing: An Explanation for New Researchers](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2816758/#!po=34.2105)
- Multiple hypothesis tests: [Tukey vs. Bonferroni vs. Scheffe: Which Test Should You Use?](https://www.statology.org/tukey-vs-bonferroni-vs-scheffe/)

### Significance testing (Fisher's approach)
- [An investigation of the false discovery rate and the misinterpretation of p-values](https://royalsocietypublishing.org/doi/pdf/10.1098/rsos.140216)

### Hypothesis testing (Neyman-Pearson's approach)
- [Mathematical Justification of Introductory Hypothesis Tests and Development of Reference Materials](https://digitalcommons.usu.edu/cgi/viewcontent.cgi?httpsredir=1&article=1014&context=gradreports)

## Estimation by sampling
Non-deterministic methods to estimate expectations of a given probability distribution (a.k.a. Monte Carlo integration)
- Uniform sampling
- Importance sampling: also used a variance-reduction technique


# Sampling methods
Methods to generate samples from a given probability distribution
- Inverse transform sampling: given the cumulative distribution function
- Rejection sampling
- Markov Chain Monte Carlo
  - ...
  - ...
  - ...

Educational
- [Visualization of random sampling techniques](https://chi-feng.github.io/mcmc-demo/app.html), sample from an N-dimensional probability density function

## Sample statistics
### Unweighted statistics
- ...
### Weighted statistics
- [Weighted percentiles (including median)](http://kochanski.org/gpk/code/speechresearch/gmisclib/gmisclib.weighted_percentile-module.html), implementation

## Estimating distribution of sample estimates
[Resampling techniques](https://en.wikipedia.org/wiki/Resampling_(statistics)#)
- Jacknife [Quenouille (1949)]: resample all n subsamples of size n-1  (useful for variance and bias estimation)
- Bootstrap [Efron (1979)]:  resampling *with replacement* from the original sample *at the same sample size* 
  - [Bootstraping dependent data](https://books.google.es/books?id=e4f8sqm439UC&printsec=frontcover#v=onepage&q&f=false):
    - Non-overlapping circular bootstrap (NBB) & Moving block bootstrap (MBB) (first and last observations are sampled less frequently)
    - Circular block bootstrap: glue start and end together and perform MBB
    - Stationary block bootstrap: stochastic blocklengths
- Subsampling [Politis and Romano (1994)]: resampling *without replacement* from the original sample *at smaller than the original sample size*
  - A comparison of [bootstrap and subsampling](http://www.stat.umn.edu/geyer/5601/notes/sub.pdf)
- Permutation tests: resampling *without replacement* from the original sample *at the same sample size*
