# Programming
## Language learning
### Python
- [es] [Guía de aprendizaje de Python by Guido Van Rossum](http://es.tldp.org/Tutoriales/Python/tut.pdf)
- [es] [Python para todos by Raúl González Duque](http://edge.launchpad.net/improve-python-spanish-doc/0.4/0.4.0/+download/Python%20para%20todos.pdf)

### C
- A Crash Course in C: Appendix A of [this book](http://hades.mech.northwestern.edu/images/e/e3/EmbeddedComputingMechatronicsSampleChapters.pdf) + [video lectures](https://www.youtube.com/playlist?list=PLggLP4f-rq02gmlePH-vQJ8PF6hyf08CN)
## Software design
- [UML basics:The class diagram - An introduction to structure diagrams in UML 2](https://www.ibm.com/developerworks/rational/library/content/RationalEdge/sep04/bell/index.html)

## JIT compiling
- [Numba architecture](http://numba.pydata.org/numba-doc/dev/developer/architecture.html)

## Building
### Tools
- [Microsoft's `nmake`](https://docs.microsoft.com/en-us/cpp/build/nmake-reference)
- [MinGW coding under Windows (C, C++, OpenMP, MPI)](http://www.math.ucla.edu/~wotaoyin/windows_coding.html)

### Educational resources
- [Compiling, assembling and linking](https://www.youtube.com/watch?v=N2y6csonII4)
- [Types of libraries, naming, resolution](https://en.wikipedia.org/wiki/Library_%28computing%29)

### Dependency viewer 
#### Executable files, object code, libraries
Including: 
- Matlab MEX files
- Python extensions (.so on Linux, .pyd on Windows)

##### Windows
- [dependencywalker](http://dependencywalker.com/), old
- [lucasg/Dependencies](https://lucasg.github.io/Dependencies/), new
- [Microsoft's `dumpbin` tool](https://docs.microsoft.com/es-es/cpp/build/reference/dumpbin-reference) (run from the Visual Studio command prompt), for [COFF](https://en.wikipedia.org/wiki/COFF)/[PE](https://en.wikipedia.org/wiki/Portable_Executable) files
  ```
  dumpbin /dependents <your_file>
  ```
##### Linux
- `ldd`

##### MacOSX
- `otool -L <filename>`

#### Java
- [depfind](http://depfind.sourceforge.net/)
