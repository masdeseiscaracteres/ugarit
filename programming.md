# Programming
## Software design
- [UML basics:The class diagram - An introduction to structure diagrams in UML 2](https://www.ibm.com/developerworks/rational/library/content/RationalEdge/sep04/bell/index.html)

## JIT compiling
- [Numba architecture](http://numba.pydata.org/numba-doc/dev/developer/architecture.html)

## Building
### Tools
- [Microsoft's `nmake`](https://docs.microsoft.com/en-us/cpp/build/nmake-reference)
- [MinGW coding under Windows (C, C++, OpenMP, MPI)](http://www.math.ucla.edu/~wotaoyin/windows_coding.html)

### Educational resources
- [Types of libraries, naming, resolution](https://en.wikipedia.org/wiki/Library_%28computing%29)

### Dependency viewer 
#### Executable files, object code, libraries
Including: 
- Matlab MEX files
- Python extensions (.so on Linux, .pyd on Windows)

##### Windows
- [dependencywalker](http://dependencywalker.com/), old
- [lucasg/Dependencies](https://lucasg.github.io/Dependencies/), new
- [Microsoft's `dumpbin` tool](https://docs.microsoft.com/es-es/cpp/build/reference/dumpbin-reference) (run from the Visual Studio command prompt)
  ```
  dumpbin /dependents <your_file>
  ```
##### Linux
- `ldd`

##### MacOSX
- `otool -L <filename>`

#### Java
- [depfind](http://depfind.sourceforge.net/)
