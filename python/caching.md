# Generic serialization/deserialization
- [pickle](https://docs.python.org/3/library/pickle.html)
- [cloudpickle](https://github.com/cloudpipe/cloudpickle/)
- [dill](https://github.com/uqfoundation/dill/)

# Python object storage/caching
- [shelve](https://docs.python.org/3/library/shelve.html), built-in
- [chest](https://github.com/blaze/chest)
- [shove](https://bitbucket.org/lcrees/shove/src)
- [cachey](https://github.com/dask/cachey)
- [bplustree](https://github.com/NicolasLM/bplustree)
- [klepto](https://github.com/uqfoundation/klepto)
- [pickleDB](https://pythonhosted.org/pickleDB/)
- [rlite](https://github.com/seppo0010/rlite-py), rlite is to Redis what SQLite is to SQL databases

# Generic hashing
- built-in `hash` function (only for the so-called [hashable](https://docs.python.org/3/glossary.html#term-hashable) objects)
- `from joblib.hashing import hash`
- `from dask.base import tokenize`
