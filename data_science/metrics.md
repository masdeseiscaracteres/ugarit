
# Machine Learning Metrics
## Statistical association
- Odds ratio: quantifies the strength of the association between two binary variables (usually represented as an 2x2 contigency table).
- [Risk difference](https://en.wikipedia.org/wiki/Risk_difference): quantifies the strength of the association between two binary variables (usually represented as an 2x2 contigency table). Common in medical studies.
- [Relative risk](https://en.wikipedia.org/wiki/Relative_risk): quantifies the strength of the association between two binary variables  (usually represented as an 2x2 contigency table). Common in medical studies.
- Correlation: quantifies the strength of the association between two continuous variables
  - Under the null hypothesis of zero correlation and when both variables follow uncorrelated normal distributions, the correlation coefficient divided by its standard deviation follows a Student's t-distribution (more info [here](https://en.wikipedia.org/wiki/Pearson_correlation_coefficient#Testing_using_Student's_t-distribution)). If squared, it follows a Snedecor's F-distribution. This reasoning is used [here](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.f_regression.html#sklearn.feature_selection.f_regression) to assess the correlation coefficient significance.
- [One-way analysis of variance (ANOVA)](https://en.wikipedia.org/wiki/Analysis_of_variance): measures the degree of association of a categorical variable and a continuous variable. It's based on the idea that, if there were an association, the mean value of the continuous variable should change with the value of the categorical variable. The test statistic is the ratio of the explained variance (between-class variability) over the unexplained variance (within-class variability). As the statistic is the ratio of two chi-squared distributed variables, it follows a Snedecor's F-distribution. This reasoning is used [here](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.f_classif.html).
- [Fisher's exact test](https://en.wikipedia.org/wiki/Fisher%27s_exact_test): quantifies the significance of the association between two categorical variables (usually represented as an MxN contigency table).
- [Chi-squared test](https://en.wikipedia.org/wiki/Chi-squared_test): statistical hypothesis test that is valid to perform when the test statistic is chi-squared distributed under the null hypothesis
  -  Person's chi-squared test: (aka. goodness of fit test) applied to sets of categorical data to test a null hypothesis stating that the frequency distribution of certain events observed in a sample is consistent with a particular theoretical distribution.
- Mutual information: quantifies the strength of association between two continuous or categorical variables
- 

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
  - Distance-based performance measure (DPM): [definition][1-open]
    - Normalized DPM (Normalized DPM)
- ROC AUC
  - Layman's definition: probability that a randomly chosen positive case will receive a higher score than a randomly chosen negative case
  - To-Do: Check if it is also referred to as [Swets' measure A][swets-open]
- Rank biserial correlation coefficient
  - Layman's definition: proportion of pairs favorable to the hypothesis (f) minus its complement (i.e.: the proportion that is unfavorable (u)): r = f - u
  - It can be expressed in terms of the ROC AUC
- Reciprocal rank
- Ranking-based precision and recall (See [Section 6.4 in this document][1-open])
- Marczewski-Steinhaus metric (or MZ-metric): [definition](http://matwbn.icm.edu.pl/ksiazki/cm/cm6/cm6141.pdf)


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
  - Conviction: how many times more often would X appear without Y if they were independent than the actual frequency of the appearance of X without Y. A high conviction then means that, by chance, X would show up without Y, more often than it actually happens in the observed data.

## Relationships
- AUC & Wilcoxon-Mann-Whitney U-Statistic:
  - [AUC Meets the Wilcoxon-Mann-Whitney U-Statistic by Bob Horton, Senior Data Scientist, Microsoft](https://blog.revolutionanalytics.com/2017/03/auc-meets-u-stat.html), includes probabilistic explanation of AUC at the end
- AUC distribution with error rate:
  - [AUC Optimization vs. Error Rate Minimization by Corinna Cortes and Mehryar Mohri](https://papers.nips.cc/paper/2518-auc-optimization-vs-error-rate-minimization.pdf), shows also the relationship with the Wilcoxon-Mann-Whitney U-Statistic 
- NDPM & Precision, Recall and Fallout:
  - [Measuring Retrieval Effectiveness Based on User Preference of Documents, Y.Y. Yao][1-open]


[1]: <https://dx.doi.org/10.1002/(SICI)1097-4571(199503)46:2%3C133::AID-ASI6%3E3.0.CO;2-Z> "Measuring Retrieval Effectiveness Based on User Preference of Documents, Y.Y. Yao (paid version)"
[1-open]: <http://www2.cs.uregina.ca/~yyao/PAPERS/jasis_ndpm.pdf> "Measuring Retrieval Effectiveness Based on User Preference of Documents, Y.Y. Yao (free version)"
[swets]: <https://dx.doi.org/10.1126/science.3287615> "Measuring the Accuracy of Diagnostic Systems, J.A. Swets (paid version)"
[swets-open]: <http://wixtedlab.ucsd.edu/publications/Psych%20218/Swets_1988.pdf> "Measuring the Accuracy of Diagnostic Systems, J.A. Swets (free version)"
