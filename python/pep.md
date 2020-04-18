# Important PEPs
- [PEP8](https://www.python.org/dev/peps/pep-0008/): style guide
- [PEP 526](https://www.python.org/dev/peps/pep-0526/): syntax for variable annotations

## Packaging
- [PEP 427](https://www.python.org/dev/peps/pep-0427/): wheel format naming and internals

  ```
  {distribution}-{version}(-{build tag})?-{python tag}-{abi tag}-{platform tag}.whl
  distribution-1.0-1-py27-none-any.whl
  ```
  
- [PEP 440](https://www.python.org/dev/peps/pep-0440/): version identification and dependency specification

  ```
  [N!]N(.N)*[{a|b|rc}N][.postN][.devN]
  1.0.1rc2.post456.dev34
  ```

- [PEP 508](https://www.python.org/dev/peps/pep-0508/): dependency specification (builds on PEP 440)

  ```
  requests [security,tests] >= 2.8.1, == 2.8.* ; python_version < "2.7"
  ```
  or
  ```
  pip @ https://github.com/pypa/pip/archive/1.3.1.zip#sha1=da9234ee9982d4bbb3c72346a6de940a148ea686
  ```
