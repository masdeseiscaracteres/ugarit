Build a big table indicating the following properties for each method

Type of reasoning: inductive, deductive
Type of induction: Prediction, description, prescription
Type of task: regression, classification, clustering, subgroup discovery

# Tasks & methods
## Regression
- Linear regression
  - Ordinary least squares
  - Total least squares
- Least absolute deviations regression
- [GLM, Generalized linear model](https://en.wikipedia.org/wiki/Generalized_linear_model): predicts by fitting a linear model to an arbitrary transformation of the expected value of the output variables given the input variables.
  <p align="center">
    <img height="40" src="https://render.githubusercontent.com/render/math?math={\displaystyle E(\mathbf{Y}|\mathbf{X})={\boldsymbol{\mu}}=g^{-1}(\mathbf{X}{\boldsymbol{\omega}})}">
  </p>

- LASSO regression
- Ridge regression

- Principal Components Regression: PCA + Linear regression
- [PLS regression](https://personal.utdallas.edu/~herve/Abdi-PLS-pretty.pdf) (Partial Least Squares or Projection to Latent Structures): performs a simultaneous decomposition of X and Y with the constraint that these components explain as much as possible of the covariance between X and Y. This generalizes PCA. The latent components are then used for regression.
- Gaussian process regression: [visual exploration](https://distill.pub/2019/visual-exploration-gaussian-processes/)

## Classification
### Binary classification
- Logistic regression: linear regression that explains the log-odds of the output. Equivalent to explaining the probability of the output by transforming a linear regression using a [logistic function](https://en.wikipedia.org/wiki/Logistic_function). It can also be regarded as a Generalized Linear Model where the link function is a logit function.
  <p align="center">
    <img height="40" src="https://render.githubusercontent.com/render/math?math=\log\left({\frac{p}{1-p}}\right)=\mathbf{x}^T{\boldsymbol{\omega}}">
  </p>  
- Probit regression: restrict linear regression output to the [0,1] interval using the CDF of the normal distribution. It can also be regarded as a Generalized Linear Model where the link function is the inverse CDF of a normal distribution.
  <p align="center">
    <img height="40" src="https://render.githubusercontent.com/render/math?math=\Phi^{-1}(p)=\mathbf{x}^T{\boldsymbol{\omega}}">
  </p> 

- FDA (Fisher Discriminant Analysis)
- LDA (Linear Discriminant Analysis)
- QDA (Quadratic Discriminant Analysis)
- RDA (Regularized Discriminant Analysis): Friedman 1989
- [SVC (Support Vector Classifier)](http://www.robots.ox.ac.uk/~az/lectures/ml/lect2.pdf)
- Nearest centroids
- [NSC (Nearest Shrunken Centroids)](http://statweb.stanford.edu/~tibs/ftp/STS040.pdf)
  - It is related to LDA, RDA, and Nearest Centroids as described in the original paper.

### Multi-class classification
- Naive Bayes
- One-vs-all or one-vs-one extensions of FDA, LDA, QDA

### Multi-label classification
- ...


## Ordinal regression/Ordinal classification
- [Logistic Ordinal Regression](http://fa.bianp.net/blog/2013/logistic-ordinal-regression/)

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
- [Elastic map](https://en.wikipedia.org/wiki/Elastic_map)
- [Corex (Correlation Explanation)](https://github.com/gregversteeg/bio_corex/): searches for a set of latent factors that best explain the correlations in the data as measured by multivariate mutual information.

## Multi-criteria decision making
- [TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)](http://www.mcdm.ue.katowice.pl/files/papers/mcdm11(6)_11.pdf)
- [AHP (Analytic Hierarchy Process)](https://en.wikipedia.org/wiki/Analytic_hierarchy_process)
- [Rank aggregation](http://www.cse.msu.edu/~cse960/Papers/games/rank.pdf)
  - Borda count
  - Footrule
  -
  
## Survival analysis
...

## Subgroup discovery
Subgroup discovery attempts to search relations between different properties or variables of a set with respect to a target variable. Due to the fact that subgroup discovery is focused in the extraction of relations with interesting characteristics, it is not necessary to obtain complete but partial relations.

## Clustering
- ...

# Comparisons
- [Partial least squares vs Principal Components regression](https://www.mathworks.com/help/stats/examples/partial-least-squares-regression-and-principal-components-regression.html)
- [Eigenproblems in Pattern Recognition](http://www.ofai.at/~roman.rosipal/Papers/eig_book04.pdf): CCA, PCA, PLS, LR, FDA (LDA) and its *kernelized* counterparts as eigendecomposition problems
- [Gini index vs Shannon entropy as impurity metrics](https://www.unine.ch/files/live/sites/imi/files/shared/documents/papers/Gini_index_fulltext.pdf)
- [The probabilistic explanation of LDA, QDA, RDA](http://www.strimmerlab.org/courses/2005-06/seminar/slides/daniela-2x4.pdf), a different approach to the optimization-based conventional one
- Técnicas de Análisis Estadístico Multivariado Basadas en Estadísticos de Segundo Orden
  - [PCA, PLS, MLR, CCA](https://ocw.unican.es/pluginfile.php/1456/course/section/1891/2%20-%20MVSA_SOS.pdf): different formulation and comparison of techniques
  - [ICA, kernel methods](https://ocw.unican.es/pluginfile.php/1456/course/section/1891/3%20-%20MVSA_HOS.pdf )
