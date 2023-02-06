# Data science libraries
## Python
### Numerical computations
- [numpy](https://numpy.org/): the flagship linear algebra/numerical computation library for Python.
- [jax](https://github.com/google/jax): "numpy" for CPU, GPU and TPU + composable numerical function transformations (includes autodifferentiation, JIT compilation, auto-vectorization, etc.)
- [numba](http://numba.pydata.org/): JIT compilation of a subset of numpy operations
- [blis](https://github.com/flame/blis): software framework for instantiating high-performance BLAS-like dense linear algebra libraries.

### Machine learning
#### General purpose
- scikit-learn
- keras: deep learning framework.  
  Can use any of these as backend:
  - tensorflow
  - ~~theano~~ -> aesara
- torch
- [patsy](https://patsy.readthedocs.io/en/latest/index.html): extensible formula mini-language to describe statistical models and building design matrices

#### Variable encoding
- [Category Encoders](https://contrib.scikit-learn.org/category_encoders/): scikit-learn contrib project including several transformers for encoding categorical variables into numeric values according to different techniques.
- [OptBinning](http://gnpalencia.org/optbinning/): solves the optimal discretization of a variable into bins given a discrete or continuous numeric target.

#### Interpretability
- [Alibi](https://github.com/SeldonIO/alibi): model explanations and confidence

#### Graphs
- [StellarGraph](https://github.com/stellargraph/stellargraph): machine-learning on graphs
- [GEM: Graph Embedding Methods](https://github.com/palash1992/GEM)
- [GraSPy: Graph Statistics in Python](https://graspy.neurodata.io/): model fitting, random graph simulation, adjacency spectral embed, ...

#### Recommender systems
- [Implicit](https://implicit.readthedocs.io/en/latest/index.html)
- [MLxtend](http://rasbt.github.io/mlxtend/), see 'frequent_patterns' section
- [scikit-surprise](http://surpriselib.com/)

#### Association rule & frequent set mining
- [pyfim](http://www.borgelt.net/pyfim.html)

#### Duplicate detection, similarity/fuzzy data matching, record linkage or entity resolution 
- [Dedupe](https://github.com/dedupeio/dedupe), by dedupe.io
- [faiss](https://github.com/facebookresearch/faiss), by Facebook research
- [splink](https://github.com/moj-analytical-services/splink)

#### Survival analysis
- [Lifelines](https://lifelines.readthedocs.io/en/latest/index.html)

#### Time series analysis
- [STL decompositions](https://pypi.org/project/stldecompose/)
- [statsmodels.tsa](https://www.statsmodels.org/stable/tsa.html): basic methods

#### Text-like processing
Generic
- [Spark NLP](https://nlp.johnsnowlabs.com/docs/en/quickstart), one of the most complete NLP toolboxes
- [spacy](https://spacy.io/), lots of out-of-the-box features for NLP. Also provides a pipeline class which makes it easy to construct sophisticated statistical models based on other libraries for a variety of NLP problems.
  - Some models include embeddings (are attached to each token as attributes)  
  - [textacy](https://github.com/chartbeat-labs/textacy), processing steps to be conducted before and after Spacy pipelines.
- [nltk](https://www.nltk.org/)
- [CoreNLP](https://stanfordnlp.github.io/CoreNLP/)
- Hugging Face
  - [transformers](https://github.com/huggingface/transformers) state-of-the-art NLP for PyTorch and TensorFlow 2.0 (BERT, GPT-2, etc.).

- [polyglot](https://github.com/aboSamoor/polyglot)
- [Gensim](https://radimrehurek.com/gensim/index.html): a library for topic modelling, word embedding, document indexing and similarity retrieval.
- [LexNLP](https://lexpredict-lexnlp.readthedocs.io): a library for working with real, unstructured legal text.
- [Mathy](https://mathy.ai/): reinforcement learning framework to transform mathematical expressions. Interesting way to encode mathematical expressions abstract syntax trees.

Preprocessing
- Contractions
  - [pycontractions](https://github.com/ian-beaver/pycontractions)
  - [contractions](https://pypi.org/project/contractions/)
- Numbers to words and the other way around 
  - [num2words](https://pypi.org/project/num2words/)
- Emojis
  - [emoji](https://github.com/carpedm20/emoji/)

Named-entities recognition (NER)
- [Duckling](https://duckling.wit.ai): identify dates/times, temperatures, amounts of money, phone numbers. Written in Clojure. Wrappers available for Python.
- [pypostal](https://github.com/openvenues/pypostal): parse & normalize addresses in every language, everywhere. Python wrapper of [libpostal](https://github.com/openvenues/libpostal).
- [FlashText](https://github.com/vi3k6i5/flashtext): replace keywords in sentences or extract keywords from sentences faster than using loops or regular expressions.

Keyword extraction
- [https://github.com/LIAAD/yake](https://github.com/LIAAD/yake): includes references to other libraries solving the same task

Distance metrics
- [abydos](https://abydos.readthedocs.io/en/latest/abydos.html): library for NLP and information retrieval. `abydos.distance` contains a huge collection of string distance functions.
- [fuzzywuzzy](https://github.com/seatgeek/fuzzywuzzy): fuzzy string matching based on Levenshtein distance.
- [rapidfuzz](https://github.com/maxbachmann/rapidfuzz): faster MIT licensed alternative to `fuzzywuzzy'.
- [regex](https://bitbucket.org/mrabarnett/mrab-regex/): regex implementation compatible with Python's built-in `re` module with some additional functionality such as fuzzy matching. 

Matching
- [PolyFuzz](https://maartengr.github.io/PolyFuzz/): fuzzy string matching, grouping. Easy to use and to extend with custom models.

Language detection
- [langdetect](https://github.com/Mimino666/langdetect)
- [spacy-langdetect](https://spacy.io/universe/project/spacy-langdetect): pipeline component wrapping `langdetect` under the hood
- [FastText](https://fasttext.cc/): offers the fastest and one of the most-accurate language detection modules
- [langid.py](https://github.com/saffsd/langid.py): intermediate speed and accuracy

### Outlier detection
- [pyod](https://github.com/yzhao062/pyod/)

### Automatic differentiation
- [jax](https://github.com/google/jax) (see description above)
- [Tangent](https://github.com/google/tangent): source-to-source automatic differentiation

### AutoML
- [Microsoft NNI (Neural Network Intelligence)](https://github.com/microsoft/nni)

### Probabilistic models & probabilistic programming
- [hmmlearn](https://hmmlearn.readthedocs.io/en/latest/index.html): sklearn API for Hidden Markov Models (Gaussian, Gaussians mixture & Multinomial emissions) 
- [Pomegranate](https://github.com/jmschrei/pomegranate): probabilistic models ranging from individual probability distributions to compositional models such as Bayesian networks, Markov chains and hidden Markov models.

- PyMC
  - [PyMC3](https://docs.pymc.io/): probabilistic programming language with Theano (with JAX implementations) as computational backend.
  - ~PyMC4~: experiment to use Tensorflow as computational backend. Development stopped in favor of adding JAX implementations to PyMC3 + Theano.
- [TensorFlow Probability](https://www.tensorflow.org/probability): probabilistic programming with Tensorflow as computation backend.
- [Pyro](http://pyro.ai/): probabilistic programming language with PyTorch as computational backend.
  - [NumPyro](http://num.pyro.ai): Pyro with numpy as computational the backend
- [Stan](https://mc-stan.org/): probabilistic programming language and platform
  - [PyStan](https://pystan.readthedocs.io/en/latest/): a Python wrapper for Stan, a package for Bayesian inference using the No-U-Turn sampler, a variant of Hamiltonian Monte Carlo (HMC).
  - [CmdStanPy](https://pycmdstan.readthedocs.io/en/latest/): lightweight pure-Python interface to CmdStan (command line interface of Stan)
- Edward
  - [Edward](https://github.com/blei-lab/edward): Python library for probabilistic modeling, inference, and criticism. 
  - [Edward2](https://github.com/google/edward2): a simple probabilistic programming language
  
Samplers
- [emcee](https://emcee.readthedocs.io/en/stable/):  pure-Python implementation of Goodman & Weare’s Affine Invariant Markov chain Monte Carlo (MCMC) Ensemble sampler

### Exploratory data analysis

- [sweetviz](https://github.com/fbdesignpro/sweetviz)
- [pandas-profiling](https://github.com/pandas-profiling/pandas-profiling)
- [lux](https://github.com/lux-org/lux/)
- [atoti](https://www.atoti.io/): BI analytics platform

Missing data analysis:
- [missingno](https://github.com/ResidentMario/missingno)

### Visualization
- [Compilation of tools](https://pyviz.org/tools.html)
- Graphs
  - [Daft](https://docs.daft-pgm.org/en/latest/): probabilistic graphical models
- Density plot
  - [mpl-scatter-density](https://github.com/astrofrog/mpl-scatter-density): matplotlib-based fast density plot
- Set intersection
  - [UpSet](https://caleydo.org/tools/upset/): visualizing intersecting sets
  - [pyvenn](https://github.com/tctianchi/pyvenn): matplotlib-based Venn diagram for 2 to 6 sets
- Tables
  - [VisiData](https://www.visidata.org/): Excel-like command-line utility to quickly review large tabular datasets
- General-purpose charting tools
  - [Apache ECharts](https://echarts.apache.org): Javascript library featuring a lot of different out-of-the-box graph types.
- Model analysis
  - [ArviZ](https://arviz-devs.github.io/arviz/index.html): exploratory analysis of Bayesian models
  - [pyLDAvis](https://github.com/bmabey/pyLDAvis): interactive topic-modelling visualization

### Synthetic data generation
- [Synthetic Data Vault](https://sdv.dev/): synthesize data using GANs
- [Faker](https://faker.readthedocs.io/en/stable/): package that generates fake data (includes community-generated data generators)

### Annotation/Labelling
- Images
  - [cvat](https://cvat.org/)
- Text
  - [brat](http://brat.nlplab.org/)
- Generic
  - [diffgram](https://diffgram.com): image, video, text, 3D, geo & more

### Workflow & model management
- [Kedro](https://kedro.readthedocs.io/en/stable/)
- [MLFlow](https://mlflow.org/docs/latest/index.html): open source platform for managing the end-to-end machine learning lifecycle (i.e. tracking experiment parameters and results, packaging, deploying, version control)
- [Cortex: deploy ML models in production](https://www.cortex.dev/): an open-source alternative to Amazon SageMaker
- [Neptune.ai](https://neptune.ai/): experiment tracking/managing/monitoring service. Has a free tier for personal and academic/research use.
- [Weights & biases](https://wandb.ai/): experiment tracking, dataset versioning, etc. Has a free tier for public and private projects.
- [gradio](https://gradio.app): quickly create customizable UI components around your TensorFlow, PyTorch models, or arbitrary Python functions.

### Parallel computation
- [dask](https://dask.org/)
- [tuplex](https://tuplex.cs.brown.edu/)

