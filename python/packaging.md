# Python packaging guides
## The definitive guide to private dependencies in Python packages
When working with private python packages (those not available on PyPI), we may encounter problems when including them as dependencies of another package.
This guide covers two common cases for private dependencies:
- How to include them in a `setup.py` file.
- How to include them in a `requirements.txt` file.

### How to include private dependencies in a setup.py file
First of all, private dependencies must be specified as any other dependency in the `install_requires` argument of the `setup()` function.

```
setup(
    ...
    install_requires= [
        private_package>=1.0
        ]
    ...
)
```

As with PyPI packages, any dependency specifier is allowed. These are the official references: 
- Complete grammar of dependency specifications ([PEP 508](https://www.python.org/dev/peps/pep-0508/))
- Version specifiers format ([PEP 404](https://www.python.org/dev/peps/pep-0440/))

Then, we need to include the `dependency_links` argument of the `setup()` and populate it with the
URL where our private packages can be found.

```
setup(
    ...
    dependency_links=[
        'git+http://github.com/user/repo/tarball/master#egg=private_package-1.0'
        ]
    ...
)
```

Some considerations:
- In the rather common case of a VCS checkout, you should also append `#egg=project-version` in order to identify which package 
and version that checkout refers to. If not sure about version, it is safer to indicate 0: https://github.com/pypa/pip/issues/3610#issuecomment-283578756
- Other than VCS URLs are also allowed as `dependency_links`: https://setuptools.readthedocs.io/en/latest/setuptools.html#dependencies-that-aren-t-in-pypi

Last, when calling `pip install` we must not forget to tell `pip` to parse the `dependency_links` section in the `setup.py` file. That is:
```
pip install --process-dependency-links <...>
```

### How to include private dependencies in a requirements file (usually requirements.txt)
When including the private dependency into the `requirements.txt` file, you have two options:
1. Specify the URL of our private dependency.
2. Specify just the name (and version) of the package and add one of the following options to the top of the file:
```
  --extra-index-url <url>     Extra URLs of package indexes to use in addition
                              to --index-url. Should follow the same rules as
                              --index-url.
  -f, --find-links <url>      If a url or path to an html file, then parse for
                              links to archives. If a local path or file://
                              url that's a directory, then look for archives
                              in the directory listing.
```

Then, the rest of the installation is done as usual:
```
pip install -r requirements.txt
```

### Using PEP 508 URL dependencies (`package @ url` syntax)
- Direct URL links can be used in requirements files since `pip>=18.0`.
- It is expected that `pip>=18.1` will support PEP 508 URL dependencies in the `setup.py` file.

### Other considerations
- If your private packages are hosted in a server using self-signed certificates or no certificates at all, 
add `--trusted-host <hostname>` to `pip install`

- To include data files, scripts, tests, etc.:
  - http://python-packaging.readthedocs.io/en/latest/index.html
  - http://setuptools.readthedocs.io/en/latest/setuptools.html
  
## Where to find binaries for Python packages
### Pip wheels
- Official Python repositories
  - [PyPi](https://pypi.python.org), ([`simple` index](https://pypi.python.org/simple/))
- Unofficial repositories
  - [Unofficial Windows binaries for third-party Python extension packages by Christoph Gohlke](https://www.lfd.uci.edu/~gohlke/pythonlibs/)

### Conda recipes
- [Anaconda recipes](https://github.com/ContinuumIO/anaconda-recipes)
- Community recipes
  - [Conda recipes](https://github.com/conda/conda-recipes), **deprecated** collection
  - [Conda-forge feedstocks (recipes +  CI +  upload to conda-forge channel)](https://github.com/conda-forge/feedstocks)
- User recipes
  1. Search for the package in anaconda.org
  2. Identify the user channel in which the package is available for your platform
  3. Install
    ```
    conda install -c <channel_name> <package_name>
    ```

### Hints to build your own conda-forge recipes
- Where should binaries (executables, libraries, etc.) go? [Answer](https://github.com/ContinuumIO/anaconda-issues/issues/233#issuecomment-69089266)
- [Helpful conda links @ conda-forge wiki](https://github.com/conda-forge/staged-recipes/wiki/Helpful-conda-links)

