# Data science
## Glossary
- Active learning: special case of machine learning in which a learning algorithm is able to interactively query the user to obtain the desired outputs at new data points
- Transfer learning: machine learning technique where a model trained on one task is re-purposed on a second related task
- Federated learning: machine learning setting where the goal is to train a high-quality centralized model with training data distributed over a large number of clients each with unreliable and relatively slow network connections

## Visualization
### Books
- [The Visual Display of Quantitative Information by Edward Tufte](https://books.google.es/books/about/The_visual_display_of_quantitative_infor.html?id=tWpHAAAAMAAJ)
- [The Grammar of Graphics by Leland Wilkinson](https://books.google.es/books/about/The_Grammar_of_Graphics.html?id=_kRX4LoFfGQC)

### Galleries
- [Data Viz Project](http://datavizproject.com/function/comparison/), language agnostic
- [from Data to Viz](https://www.data-to-viz.com/), taxonomy of graph types, refers to Python, R, and D3.js graph galleries.
- [D3.js gallery](https://github.com/d3/d3/wiki/Gallery), Javascript
- [Visual Vocabulary](https://gramener.github.io/visual-vocabulary-vega/), Vega edition, inspired in the Financial Times Visual Vocabulary poster

### Libraries
#### Low-level
Ideal for custom communication plots.
- matplotlib: Python
- Plotly.js: Javascript, built on top of React.js, D3.js and WebGL, wrappers for Python (plotly.py), R (plotly.R)
- Vega: a visualization grammar in JSON, includes a Javascript runtine API and wrappers for Python (Altair)
- D3.js: Javascript

#### High-level
Ideal for fast exploration plots.
- seaborn: Python, built on top of matplotlib
- gadfly: Julia
- ggplot2: R
- [Plotly Express](https://plotly.github.io/plotly_express/)

##### Dashboards
- [Panel](https://panel.pyviz.org/)
- [Voilà](https://github.com/QuantStack/voila), turns Jupyter notebooks into standalone web applications

## Distance metrics
- [textdistance](https://github.com/orsinium/textdistance), Python package

## Machine-learned rankings

## Regression
- [Linear regression -> Bayesian regression -> Gaussian processes](https://www.cs.ubc.ca/labs/lci/mlrg/slides/GaussianProcessses.pdf)

## Classification

### Binary classification name equivalences
Generic names
- P(1|1): TPR
- P(1|0): FPR
- P(0|1): FNR
- P(0|0): TNR

Diagnosis
- P(1|1): sensitivity
- P(0|0): specificity

Sales:
- P(1|1): hit rate
- P(0|1): miss rate

Information retrieval
- P(1|1): recall
- P(1|0): fall-out

Signal detection
- P(1|1): probability of detection
- P(1|0): probability of false alarm

Statistical hyphotesis testing
- P(1|1): power (1-beta)
- P(1|0): significance level, Type I error rate (alpha)
- P(0|1): type II error rate (beta)

## Ensemble methods
### Rank-aggregation

### Bagging

### Boosting

### Stacking

## Sampling
- [Visualization of random sampling techniques](https://chi-feng.github.io/mcmc-demo/app.html), sample from an N-dimensional probability density function

## Recommender systems (RS)
- [Recommender systems, Encyclopedia of Machine Learning](http://www.prem-melville.com/publications/recommender-systems-eml2010.pdf):
  - Collaborative filtering (CF): similarity with other user ratings used to assign ratings
    - Memory-based (a.k.a. Neighborhood-based)
      - User-based: similarities between the rows of the ratings matrix
      - Item-based: similarities between the columns of the ratings matrix
    - Model-based
      > *Examples:* latent factor models, matrix factorization
  - Content-based RS: item descriptors are used to predict the rating a user would likely assign to an item
    > *Advantages/Disadvantages*: low diversity of recommended items, ineffective for new users/good for new unrated items
  - Knowledge-based RS: useful if items not purchased very often. Give recommendations based on the similarity of a user requirements and item attributes
  - Hybrid approaches
  
  

## Reproducible research
- [mybinder.org](http://mybinder.org/), visualization Jupyter Notebooks
- [everware.org](http://everware.xyz/), online execution Jupyter Notebooks
- Citable datasets
  - [zenodo.org](https://zenodo.org/), free DOI
  - [data.mendeley.com](https://data.mendeley.com), free DOI
- Embedded interactive Python/R interpreter
  - [Datacamp Light](https://github.com/datacamp/datacamp-light-wordpress)
- Online notebooks:
  - [Iodide](https://alpha.iodide.io/), notebooks featuring HTML, markdown, JS and Python in the browser (yes, Python in the browser)
  - [Google Colaboratory](https://colab.research.google.com), Jupyter notebook execution on Google Cloud servers
  
## Datasets
- [Common Crawl](http://commoncrawl.org/), raw web page data, extracted metadata and text extractions, freely accesible/dowloadable from Amazon Public Datasets  
- [Global Database of Events, Language, and Tone (GDELT) project](https://www.gdeltproject.org/), a realtime database of global society, freely accesible using Google BigQuery
- [Wifi networks](https://wigle.net/), collaboratively gathered geolocalized Wifi hotspot observations
