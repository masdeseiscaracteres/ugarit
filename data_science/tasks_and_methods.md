Build a big table indicating the following properties for each method. Or a graph showing relationships, generalizations, definitions, etc...

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
- One-vs-all(-but-one) or one-vs-one extensions of FDA, LDA, QDA
- NB ([Naive Bayes](http://web.cs.iastate.edu/~honavar/bayes-lewis.pdf))
  - MNB (Multinomial Naive Bayes): the 
  - [CNB (Complement Naive Bayes)](https://people.csail.mit.edu/jrennie/papers/icml03-nb.pdf): alternative to multinomial naive bayes that addresses some of its limitations:
    - Limitation 1: it shrinks weights for classes with few training examples. A solution is estimating the parameters using data from classes other than the one of interest. This gives rise to Complement Naive Bayes.
    - Limitation 2: features are assumed to be independent. The consequence is that the impact of classes with strong feature dependencies is larger when compared to classes with less feature dependencies. A solution is normalizing the classification weights giving rise to Weight-normalized Complement Naive Bayes.
    - Limitation 3: it doesn't model text well. 
      - A power law distribution may be a better fit. Solution: transform word frequency, for example, doing f_i'=log(d+f_i}.
      - Document frequency is not taken into account. Solution: give a lower weight to words that are common across document, for example, using TF-IDF.
      - Words are more likely to occur in longer documents. Solution: normalize word counts, for example, doing f_i'=f_i/(\sum(f_k)^2. This change has a subtle effect because, for classification, comparisons are made across classes and across documents. 

### Multi-label classification
- It can be built from many one-vs-rest models

## [Record linkage](https://en.wikipedia.org/wiki/Record_linkage) / data matching
- 

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

## Text
### Keyword extraction/text summarization
Keyword extraction and text summarization can be regarded as the same task, the only difference is that for keyword extraction we must look at the document as a word collection whereas, for text summarization, we must look at it as a sentence collection.
- [LSA (Latent Semantic Analysis)](http://www.kiv.zcu.cz/~jstein/publikace/isim2004.pdf): known as LSI (Latent Semantic Indexing) in Information Retrieval.
- TextRank: based on [PageRank](https://en.wikipedia.org/wiki/PageRank)
  1. Compute the TF-IDF matrix
  2. Compute a similarity metric among the sentences in the document. Similarity can be calculated as the correlation among TF-IDF vectors. To compute similarity among words instead of sentences we can use the number of co-ocurrences among words in a sliding window of a given size.
  3. Build a graph where each sentence is represented as a node (edge weights represent sentence similarity)
  4. Run PageRank algorithm on this graph
- [RAKE (Rapid Automatic Keyword Extraction)](https://www.researchgate.net/publication/227988510_Automatic_Keyword_Extraction_from_Individual_Documents)
- Most relevant n-grams (by relative frequency, o conditional probability)

### Text embeddings
- Word2Vec: Embedding + Logistic Regression. Input: one-hot encoded word, output: probability of words in the context of the input word (obtained by counting co-ocurrences in sliding window contexts, see [skip-gram](https://en.wikipedia.org/wiki/N-gram#Skip-gram) for possibilites, typically a n-skip-2-gram is used). Both the Logistic Regression coefficients and embedding matrix are learned during training. Usually we are interested in the embedding matrix but the classifier itself may be used for a text autocompletion task.

# Comparisons
- [Partial least squares vs Principal Components regression](https://www.mathworks.com/help/stats/examples/partial-least-squares-regression-and-principal-components-regression.html)
- [Eigenproblems in Pattern Recognition](http://www.ofai.at/~roman.rosipal/Papers/eig_book04.pdf): CCA, PCA, PLS, LR, FDA (LDA) and its *kernelized* counterparts as eigendecomposition problems
- [Gini index vs Shannon entropy as impurity metrics](https://www.unine.ch/files/live/sites/imi/files/shared/documents/papers/Gini_index_fulltext.pdf)
- [The probabilistic explanation of LDA, QDA, RDA](http://www.strimmerlab.org/courses/2005-06/seminar/slides/daniela-2x4.pdf), a different approach to the optimization-based conventional one
- Técnicas de Análisis Estadístico Multivariado Basadas en Estadísticos de Segundo Orden
  - [PCA, PLS, MLR, CCA](https://ocw.unican.es/pluginfile.php/1456/course/section/1891/2%20-%20MVSA_SOS.pdf): different formulation and comparison of techniques
  - [ICA, kernel methods](https://ocw.unican.es/pluginfile.php/1456/course/section/1891/3%20-%20MVSA_HOS.pdf )
