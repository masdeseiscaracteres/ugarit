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
- [cacheout](https://github.com/dgilland/cacheout)
- [zict](https://github.com/dask/zict)
- [bplustree](https://github.com/NicolasLM/bplustree)
- [klepto](https://github.com/uqfoundation/klepto)
- [lmdb](https://lmdb.readthedocs.io/en/release/), Python binding for the LMDB ‘Lightning’ Database
- Redis-like
  - [pickleDB](https://pythonhosted.org/pickleDB/), Redis inspired file storage
  - [rlite](https://github.com/seppo0010/rlite-py), rlite is to Redis what SQLite is to SQL databases, in-memory or on-disk storage
- MongoDB-like
  - [unqlite-python](https://github.com/coleifer/unqlite-python): key-value store + JSON document collection store in the spirit of MongoDB. Supports both in-memory and on-disk storage. Queries on the JSON document collections are conducted in a [Jx9](https://unqlite.org/jx9.html) virtual machine.
    - *Possible bug*: it doesn't free space when deleting entries.
  - [TinyDB](https://tinydb.readthedocs.io/en/latest/#): tiny document oriented database in the spirit of MongoDB. Supports both in-memory and on-disk storage but is easy to extend.
    - *Warning*: doesn't support the jsonlines format.

# Generic hashing
- built-in `hash` function (only for the so-called [hashable](https://docs.python.org/3/glossary.html#term-hashable) objects)
- `from joblib.hashing import hash`
- `from dask.base import tokenize`
