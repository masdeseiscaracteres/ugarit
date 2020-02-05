# Graph Theory
- [Interactive introduction to graph theory](https://mrpandey.github.io/d3graphTheory/index.html)

# Probability & Statistics
- [Probability and Statistics Cookbook](http://statistics.zone/)


## Statistical testing
- Two main approaches: https://en.m.wikibooks.org/wiki/Statistics/Testing_Data/Purpose
- Differences: [P Value and the Theory of Hypothesis Testing: An Explanation for New Researchers](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2816758/#!po=34.2105)

### Significance testing (Fisher's approach)
- [An investigation of the false discovery rate and the misinterpretation of p-values](https://royalsocietypublishing.org/doi/pdf/10.1098/rsos.140216)

### Hypothesis testing (Neyman-Pearson's approach)
- [Mathematical Justification of Introductory Hypothesis Tests and Development of Reference Materials](https://digitalcommons.usu.edu/cgi/viewcontent.cgi?httpsredir=1&article=1014&context=gradreports)

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
