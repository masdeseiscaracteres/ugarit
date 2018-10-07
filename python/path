# How is sys.path populated?
## What is sys.path?
It is just a list of strings that specifies the search path for modules. Refer to the [official doc](https://docs.python.org/3/library/sys.html#sys.path) for more details.

It is populated in two steps:

### Entries added on interpreter startup
The first item of this list, `sys.path[0]`, is the directory containing the script that was used to invoke the Python interpreter. If the script directory is not available (e.g. if the interpreter is invoked interactively or if the script is read from standard input), `sys.path[0]` is the empty string, which directs Python to search modules in the current directory first.

Then the entries defined in the environment variable [`PYTHONPATH`](https://docs.python.org/3/using/cmdline.html#envvar-PYTHONPATH) are appended to `sys.path`.

### Entries added by the site.py module
Afterwards, the `sys.path` is the populated by the module [`site`](https://docs.python.org/3/library/site.html) (which is automatically imported on startup, `python -S` avoids it) according to the following steps:

1. Four directories are added to the path (if they exist): 
   - [`sys.prefix`](https://docs.python.org/3/library/sys.html#sys.prefix)
   - `sys.prefix + site_packages_tail`
   - `sys.exec_prefix`
   - `sys.exec_prefix + site_packages_tail`
 
 where `site_packages_tail` is `lib/site-packages` (on Windows) or `lib/pythonX.Y/site-packages` (on Unix and Macintosh)
 
2. Search those directories for `*.pth`files and add their contents to `sys.path`. Execute also any `import ` statement.
3. Execute a `sitecustomize.py` module if it is found in the path already added to `sys.path`
4. Execute a `usercustomize.py` module if it is found in the path already added to `sys.path`

The final status of the `sys.path` variable and user-specific directories can be checked by doing:
```
python -m site
```
