# Programming
## Software design
- [UML basics:The class diagram - An introduction to structure diagrams in UML 2](https://www.ibm.com/developerworks/rational/library/content/RationalEdge/sep04/bell/index.html)

## JIT compiling
- [Numba architecture](http://numba.pydata.org/numba-doc/dev/developer/architecture.html)

## Build tools
- [Microsoft's `nmake`](https://docs.microsoft.com/en-us/cpp/build/nmake-reference)
- [MinGW coding under Windows (C, C++, OpenMP, MPI)](http://www.math.ucla.edu/~wotaoyin/windows_coding.html)

### Dependency viewer 
#### C libraries (Matlab MEX files, Python .pyd files)
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
