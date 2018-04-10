# Generic serialization/deserialization
- [pickle](https://docs.python.org/3/library/pickle.html)
- [cloudpickle](https://github.com/cloudpipe/cloudpickle/)
- [dill](https://github.com/uqfoundation/dill/)

# Python object storage/caching
- [shelve](https://docs.python.org/3/library/shelve.html), built-in persistent (file storage) key-value store, values can be arbitrary objects serialized with `pickle`. 
  - Backend: [dbm](https://docs.python.org/3/library/dbm.html#module-dbm), both keys and values restricted to byte strings
  
- [chest](https://github.com/blaze/chest), memory-cached persistent file storage, custom serialization allowed 
- [shove](https://bitbucket.org/lcrees/shove/src), custom cache and file storage, supports backend in an URI 
- [cachey](https://github.com/dask/cachey)
- [bplustree](https://github.com/NicolasLM/bplustree)
- [klepto](https://github.com/uqfoundation/klepto)
- Redis compatible
  - [pickleDB](https://pythonhosted.org/pickleDB/), Redis inspired file storage
  - [rlite](https://github.com/seppo0010/rlite-py), rlite is to Redis what SQLite is to SQL databases, in-memory or in-file storage

# Generic hashing
- built-in `hash` function (only for the so-called [hashable](https://docs.python.org/3/glossary.html#term-hashable) objects)
- `from joblib.hashing import hash`
- `from dask.base import tokenize`
