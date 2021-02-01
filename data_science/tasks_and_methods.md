# Tasks & methods
## Regression
- Linear regression
  - Ordinary least squares
  - Total least squares
- [GLM, Generalized linear model](https://en.wikipedia.org/wiki/Generalized_linear_model): predicts by fitting a linear model to an arbitrary transformation of the expected value of the output variables given the input variables.
- LASSO regression
- Ridge regression

- [PLS regression](https://personal.utdallas.edu/~herve/Abdi-PLS-pretty.pdf) (Partial Least Squares or Projection to Latent Structures)
- Principal Components Regression: PCA + Linear regression
- Gaussian process regression: [visual exploration](https://distill.pub/2019/visual-exploration-gaussian-processes/)

## Classification
### Binary classification
- Logistic regression: linear regression that explains the log-odds of the output. Equivalent to explaining the probability of the output by transforming a linear regression using a [logistic function](https://en.wikipedia.org/wiki/Logistic_function). It can also be regarded as a Generalized Linear Model where the link function is a logit function.
  <p align="center">
    <img height="40" src="https://render.githubusercontent.com/render/math?math=\log\left({\frac{p_i}{1-p_i}}\right)=\mathbf{x}_i^T{\boldsymbol{\omega}}">
  </p>  
- Probit regression: restrict linear regression output to the [0,1] interval using the CDF of the normal distribution
- FDA (Fisher Discriminant Analysis)
- LDA (Linear Discriminant Analysis)
- QDA (Quadratic Discriminant Analysis)
- RDA (Regularized Discriminant Analysis)
- [SVC (Support Vector Classifier)](http://www.robots.ox.ac.uk/~az/lectures/ml/lect2.pdf)


### Multi-class classification
- Naive Bayes
- One-vs-all or one-vs-one extensions of FDA, LDA, QDA

### Multi-label classification
- ...

## Metric learning
- ...

## Dimensionality reduction
- FDA/LDA (see binary classification): maximize projected interclass variance/intraclass variance
- PCA (Principal Components Analysis): maximize projected variance
  - Mainly concerned with preserving large pairwise distances: dissimilar points stay dissimilar
- CCA (Canonical Correlation Analysis): maximize projected correlation
- ICA (Independent Component Analysis)
- MDS (Multi-Dimensional Scaling): same as PCA but changing the way distances among high-dimensional points are computed
- ISOMAP: geodesic distances + MDS:
  - Focus on preserving small pairwise distances
- [Sammon mapping](https://en.wikipedia.org/wiki/Sammon_mapping): idea of relativizing distance functions (i.e. a small error is more important when measuring small distances than large distances) 
- LLE (Locally Linear Embeddings)
  - Focus on preserving small pairwise distances but ends up collapsing many points into the origin and compensating that by creating rays coming out of the origin
- [t-SNE (t-distributed Stochastic Neighbor Embedding)](https://www.youtube.com/watch?v=RJVL80Gg3lA), minimize KL divergence between the high-dimensional and low-dimensional distribution of all the pairs of points (idea similar to that of LLE)
  - Perplexity parameter controls the effective number of neighbors.
- [SOM (Self-Organizing Map)](https://en.wikipedia.org/wiki/Self-organizing_map)
- [Semidefinite embedding (SDE) or maximum variance unfolding (MVU)](https://en.wikipedia.org/wiki/Semidefinite_embedding)
- Laplacian eigenmaps
- UMAP
- [Corex (Correlation Explanation)](https://github.com/gregversteeg/bio_corex/): searches for a set of latent factors that best explain the correlations in the data as measured by multivariate mutual information.

## Clustering
- ...

## Multi-criteria decision making
- [TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)](http://www.mcdm.ue.katowice.pl/files/papers/mcdm11(6)_11.pdf)
- [AHP (Analytic Hierarchy Process)](https://en.wikipedia.org/wiki/Analytic_hierarchy_process)
- [Rank aggregation](http://www.cse.msu.edu/~cse960/Papers/games/rank.pdf)
  - Borda count
  - Footrule
  -
  
# Comparisons
- [Partial least squares vs Principal Components regression](https://www.mathworks.com/help/stats/examples/partial-least-squares-regression-and-principal-components-regression.html)
- [Eigenproblems in Pattern Recognition](http://www.ofai.at/~roman.rosipal/Papers/eig_book04.pdf): CCA, PCA, PLS, LR, FDA (LDA) and its *kernelized* counterparts as eigendecomposition problems
- [Gini index vs Shannon entropy as impurity metrics](https://www.unine.ch/files/live/sites/imi/files/shared/documents/papers/Gini_index_fulltext.pdf)
- [The probabilistic explanation of LDA, QDA, RDA](http://www.strimmerlab.org/courses/2005-06/seminar/slides/daniela-2x4.pdf), a different approach to the optimization-based conventional one
- Técnicas de Análisis Estadístico Multivariado Basadas en Estadísticos de Segundo Orden
  - [PCA, PLS, MLR, CCA](https://ocw.unican.es/pluginfile.php/1456/course/section/1891/2%20-%20MVSA_SOS.pdf): different formulation and comparison of techniques
  - [ICA, kernel methods](https://ocw.unican.es/pluginfile.php/1456/course/section/1891/3%20-%20MVSA_HOS.pdf )
