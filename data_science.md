# Data science
## Visualization
### Books
- [The Visual Display of Quantitative Information by Edward Tufte](https://books.google.es/books/about/The_visual_display_of_quantitative_infor.html?id=tWpHAAAAMAAJ)
- [The Grammar of Graphics by Leland Wilkinson](https://books.google.es/books/about/The_Grammar_of_Graphics.html?id=_kRX4LoFfGQC)

### Galleries
- [Data Viz Project](http://datavizproject.com/function/comparison/), language agnostic
- [The Python Graph Gallery](https://python-graph-gallery.com/), Python
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


## Recommender systems
- [Recommender systems, Encyclopedia of Machine Learning](http://www.prem-melville.com/publications/recommender-systems-eml2010.pdf):
  - Collaborative filtering (neighborhood-based & model-based)
  - Content-based recommending
  - Hybrid approaches

## Reproducible research
- [mybinder.org](http://mybinder.org/), visualization Jupyter Notebooks
- [everware.org](http://everware.xyz/), online execution Jupyter Notebooks
- Citable datasets
  - [zenodo.org](https://zenodo.org/), free DOI
  - [data.mendeley.com](https://data.mendeley.com), free DOI
- Embedded interactive Python/R interpreter
  - [Datacamp Light](https://github.com/datacamp/datacamp-light-wordpress)

## Datasets
- [Common Crawl](http://commoncrawl.org/), raw web page data, extracted metadata and text extractions, freely accesible/dowloadable from Amazon Public Datasets  
- [Global Database of Events, Language, and Tone (GDELT) project](https://www.gdeltproject.org/), a realtime database of global society, freely accesible using Google BigQuery
- [Wifi networks](https://wigle.net/), collaboratively gathered geolocalized Wifi hotspot observations
