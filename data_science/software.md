# Data science libraries
## Python
### Machine learning
#### General purpose
- scikit-learn
- tensorflow
- keras
- theano
- torch
- [patsy](https://patsy.readthedocs.io/en/latest/index.html): extensible formula mini-language to describe statistical models and building design matrices

#### Interpretability
- [Alibi](https://github.com/SeldonIO/alibi): model explanations and confidence

#### Graphs
- [StellarGraph](https://github.com/stellargraph/stellargraph): machine-learning on graphs
- [GEM: Graph Embedding Methods](https://github.com/palash1992/GEM)
- [GraSPy: Graph Statistics in Python](https://graspy.neurodata.io/): model fitting, random graph simulation, adjacency spectral embed, ...

#### Recommender systems
- [Implicit](https://implicit.readthedocs.io/en/latest/index.html)
- MLxtend
- scikit-surprise

#### Similarity & matching
- [Dedupe](https://github.com/dedupeio/dedupe), by dedupe.io
- [faiss](https://github.com/facebookresearch/faiss), by Facebook research

#### Survival analysis
- [Lifelines](https://lifelines.readthedocs.io/en/latest/index.html)

#### Text-like processing
Generic
- [Spark NLP](https://nlp.johnsnowlabs.com/docs/en/quickstart), one of the more complete NLP toolboxes
- [spacy](https://spacy.io/), lots of out-of-the-box features for NLP. Also provides a pipeline class which makes it easy to construct sophisticated statistical models based on other libraries for a variety of NLP problems.
  - [textacy](https://github.com/chartbeat-labs/textacy), processing steps to be conducted before and after Spacy pipelines.
- [nltk](https://www.nltk.org/)
- [CoreNLP](https://stanfordnlp.github.io/CoreNLP/)
- Hugging Face
  - [transformers](https://github.com/huggingface/transformers) state-of-the-art NLP for PyTorch and TensorFlow 2.0 (BERT, GPT-2, etc.).

- [polyglot](https://github.com/aboSamoor/polyglot)
- [Gensim](https://radimrehurek.com/gensim/index.html): a library for topic modelling, document indexing and similarity retrieval.
- [LexNLP](https://lexpredict-lexnlp.readthedocs.io): a library for working with real, unstructured legal text.
- [Mathy](https://mathy.ai/): reinforcement learning framework to transform mathematical expressions. Interesting way to encode mathematical expressions abstract syntax trees.

Named-entities recognition (NER)
- [Duckling](https://duckling.wit.ai): identify dates/times, temperatures, amounts of money, phone numbers. Written in Clojure. Wrappers available for Python.
- [pypostal](https://github.com/openvenues/pypostal): parse & normalize addresses in every language, everywhere. Python wrapper of [libpostal](https://github.com/openvenues/libpostal).

Distance metrics
- [abydos](https://abydos.readthedocs.io/en/latest/abydos.html): library for NLP and information retrieval. `abydos.distance` contains a huge collection of string distance functions.
- [fuzzywuzzy](https://github.com/seatgeek/fuzzywuzzy): fuzzy string matching based on Levenshtein distance.
- [rapidfuzz](https://github.com/maxbachmann/rapidfuzz): faster MIT licensed alternative to `fuzzywuzzy'.
- [regex](https://bitbucket.org/mrabarnett/mrab-regex/): regex implementation compatible with Python's built-in `re` module with some additional functionality such as fuzzy matching. 

#### Association rule & frequent set mining
- [pyfim](http://www.borgelt.net/pyfim.html)

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

### Workflow & model management
- [Kedro](https://kedro.readthedocs.io/en/stable/)
- [MLFlow](https://mlflow.org/docs/latest/index.html)
- [Cortex: deploy ML models in production](https://www.cortex.dev/): an open-source alternative to Amazon SageMaker



