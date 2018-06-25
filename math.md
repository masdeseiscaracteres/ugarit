# Graph Theory
- [Interactive introduction to graph theory](https://mrpandey.github.io/d3graphTheory/index.html)

# Probability & Statistics
- [Probability and Statistics Cookbook](http://statistics.zone/)


## Statistical testing
- Two main approaches: https://en.m.wikibooks.org/wiki/Statistics/Testing_Data/Purpose
- Differences: [P Value and the Theory of Hypothesis Testing: An Explanation for New Researchers](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2816758/#!po=34.2105)
### Significance testing (Fisher's approach)
- ...
### Hypothesis testing (Neyman-Pearson's approach)
- [Mathematical Justification of Introductory Hypothesis Tests and Development of Reference Materials](https://digitalcommons.usu.edu/cgi/viewcontent.cgi?httpsredir=1&article=1014&context=gradreports)

## Estimating distribution of sample estimates
[Resampling techniques](https://en.wikipedia.org/wiki/Resampling_(statistics)#)
- Jacknife [Quenouille (1949)]: resample all n subsamples of size n-1  (useful for variance and bias estimation)
- Bootstrap [Efron (1979)]:  resampling *with replacement* from the original sample *at the same sample size* 
- Subsampling [Politis and Romano (1994)]: resampling *without replacement* from the original sample *at smaller than the original sample size*
  - A comparison of [bootstrap and subsampling](http://www.stat.umn.edu/geyer/5601/notes/sub.pdf)
- Permutation tests: resampling *without replacement* from the original sample *at the same sample size*
