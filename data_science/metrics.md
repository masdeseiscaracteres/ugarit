
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
- ROC AUC
  - Layman's definition: probability that a randomly chosen positive case will receive a higher score than a randomly chosen negative case
- Rank biserial correlation coefficient
  - Layman's definition: proportion of pairs favorable to the hypothesis (f) minus its complement (i.e.: the proportion that is unfavorable (u)): r = f - u
  - It can be expressed in terms of the ROC AUC
- Reciprocal rank


- Precision at k: [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)
- Average Precision at k: [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)
- Recall at k: [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)
- Cumulative gain (curve) & lift curve
- Discounted cumulative gain: [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)
- Normalized discounted cumulative gain: [definition & examples](https://ils.unc.edu/courses/2013_spring/inls509_001/lectures/10-EvaluationMetrics.pdf)

For many queries:
- Mean average precision
- Mean reciprocal rank



Metrics definition: https://nlp.stanford.edu/IR-book/pdf/08eval.pdf

## Relationships
- AUC & Wilcoxon-Mann-Whitney U-Statistic:
  - [AUC Meets the Wilcoxon-Mann-Whitney U-Statistic by Bob Horton, Senior Data Scientist, Microsoft](https://blog.revolutionanalytics.com/2017/03/auc-meets-u-stat.html), includes probabilistic explanation of AUC at the end
- AUC distribution with error rate:
  - [AUC Optimization vs. Error Rate Minimization by Corinna Cortes and Mehryar Mohri](https://papers.nips.cc/paper/2518-auc-optimization-vs-error-rate-minimization.pdf), shows also the relationship with the Wilcoxon-Mann-Whitney U-Statistic 
