
# Machine Learning Metrics
## Classification
- ...
- ROC AUC

## Regression
- ...

## Ordering/Ranking

For a single query:
- Rank correlations
  - Spearman's rank correlation coefficient
  - Kendall's tau rank correlation coefficient
  - Distance-based performance measure (DPM): [definition](https://core.ac.uk/download/pdf/191177829.pdf)
    - Normalized DPM (Normalized DPM)
- ROC AUC
  - Layman's definition: probability that a randomly chosen positive case will receive a higher score than a randomly chosen negative case
  - To-Do: Check if it is also referred to as [Swets's measure A](https://apps.dtic.mil/dtic/tr/fulltext/u2/656340.pdf) 
- Rank biserial correlation coefficient
  - Layman's definition: proportion of pairs favorable to the hypothesis (f) minus its complement (i.e.: the proportion that is unfavorable (u)): r = f - u
  - It can be expressed in terms of the ROC AUC
- Reciprocal rank
- Ranking-based precision and recall (See [Section 6.4 in this document](https://core.ac.uk/download/pdf/191177829.pdf))
- Marczewski-Steinhaus metric (or MZ-metric):[definition](http://matwbn.icm.edu.pl/ksiazki/cm/cm6/cm6141.pdf)


- Precision at k: [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)
- Average Precision at k: [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)
- Recall at k: [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)
- Cumulative gain (curve) & lift curve
- Discounted cumulative gain: [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)
  - For a choice of discounting factors (or grade-to-gain mappings) see [Sec. 4. Results C2](http://ir.ii.uam.es/pubs/irj2020.pdf)
- Normalized discounted cumulative gain (NDCG): [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)
- Rank-biased precision (RBP): [definition](https://dl.acm.org/doi/10.1145/1416950.1416952)
- Half-life utility: [definition](https://doi.org/10.1145/963770.963772)
  - Layman's definition: The likelihood that a user will view each successive item is described with an exponential decay function, where the strength of the decay is described by a half-life parameter. Also, the rank of the item on the list such that there is a 50% chance that the user will view that item.

For many queries: the metrics obtained for each query need to be aggregated for all queries
- Arithmetic mean
  - Weighted/unweighted 
- Geometric mean
- Commonly used aggregations:
  - Mean average precision
  - Mean reciprocal rank

Metrics definition: https://nlp.stanford.edu/IR-book/pdf/08eval.pdf

## Topic modelling
- Fit metrics
  - Log likelihood
  - Log perplexity 
- Coherence metrics: important words for a topic, frequently appear together 
  - UCI coherence score
  - UMass coherence
  - NPMI (Normalized Pointwise Mutual Information)

## Probability distributions
- [Total variation distance](https://en.wikipedia.org/wiki/Total_variation_distance_of_probability_measures)
- Kullback-Leibler divergence
- Jensen–Shannon divergence: symmetrized and smoothed version of the Kullback–Leibler divergence
- Hellinger distance
- Gini impurity: the probability of incorrectly classifying a randomly chosen element in the dataset if it were randomly labeled according to the class distribution in the dataset.
  - In other words: suppose we randomly pick a datapoint in our dataset, then randomly classify it according to the class distribution in the dataset. What’s the probability we classify the datapoint incorrectly?

## Association rule mining
- [Huge compilation of metrics to evaluate association rules](https://michael.hahsler.net/research/association_rules/measures.html)
  - Conviction: how many times more often would X appear without Y if they were independent than the actual frequency of the appearance of X without Y. 

## Relationships
- AUC & Wilcoxon-Mann-Whitney U-Statistic:
  - [AUC Meets the Wilcoxon-Mann-Whitney U-Statistic by Bob Horton, Senior Data Scientist, Microsoft](https://blog.revolutionanalytics.com/2017/03/auc-meets-u-stat.html), includes probabilistic explanation of AUC at the end
- AUC distribution with error rate:
  - [AUC Optimization vs. Error Rate Minimization by Corinna Cortes and Mehryar Mohri](https://papers.nips.cc/paper/2518-auc-optimization-vs-error-rate-minimization.pdf), shows also the relationship with the Wilcoxon-Mann-Whitney U-Statistic 
- NDPM & Precision, Recall and Fallout:
 - [Measuring Retrieval Effectiveness Based on User Preference of Documents, Y.Y. Yao](https://core.ac.uk/download/pdf/191177829.pdf)
