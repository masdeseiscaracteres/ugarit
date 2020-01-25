# Tasks & methods
## Regression
- Linear regression
  - Ordinary least squares
  - Total least squares
- [GLM, Generalized linear model](https://en.wikipedia.org/wiki/Generalized_linear_model)
- LASSO regression
- Ridge regression

- [PLS regression](https://personal.utdallas.edu/~herve/Abdi-PLS-pretty.pdf) (Partial Least Squares or Projection to Latent Structures)
- Principal Components Regression: PCA + Linear regression

## Classification
### Binary classification
- Logistic regression: restrict linear regression output to the [0,1] interval using a [logistic function](https://en.wikipedia.org/wiki/Logistic_function)
- Probit regression: restrict linear regression output to the [0,1] interval using the CDF of the normal distribution
- FDA (Fisher Discriminant Analysis)
- LDA (Linear Discriminant Analysis)
- QDA (Quadratic Discriminant Analysis)
- RDA (Regularized Discriminant Analysis)


### Multi-class classification
- Naive Bayes
- One-vs-all or one-vs-one extensions of FDA, LDA, QDA

## Dimensionality reduction
- FDA/LDA (see binary classification): maximize projected interclass variance/intraclass variance
- PCA (Principal Components Analysis): maximize projected variance
- CCA (Canonical Correlation Analysis): maximize projected correlation
- ICA (Independent Component Analysis)
- ISOMAP: geodesic distances + MDS
- LLE (Locally Linear Embeddings)
- MDS (Multi-Dimensional Scaling)
- t-SNE (T-distributed Stochastic Neighbor Embedding)
- [SOM (Self-Organizing Map)](https://en.wikipedia.org/wiki/Self-organizing_map)

# Comparisons
- [Partial least squares vs Principal Components regression](https://www.mathworks.com/help/stats/examples/partial-least-squares-regression-and-principal-components-regression.html)
- [Eigenproblems in Pattern Recognition](http://www.ofai.at/~roman.rosipal/Papers/eig_book04.pdf): CCA, PCA, PLS, LR, FDA (LDA) and its *kernelized* counterparts as eigendecomposition problems
- [Gini index vs Shannon entropy as impurity metrics](https://www.unine.ch/files/live/sites/imi/files/shared/documents/papers/Gini_index_fulltext.pdf)
- [The probabilistic explanation of LDA, QDA, RDA](http://www.strimmerlab.org/courses/2005-06/seminar/slides/daniela-2x4.pdf), a different approach to the optimization-based conventional one
