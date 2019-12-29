# Rounding
- AMS article on apportionment: [part 1](http://www.ams.org/publicoutreach/feature-column/fcarc-apportion1) & [part 2](http://www.ams.org/publicoutreach/feature-column/fcarc-apportionii1)
- [voting](https://github.com/crflynn/voting): Python package for apportionment 

# Graphs
- See https://algs4.cs.princeton.edu/cheatsheet/ (graph algorithms section) for more info
- ["Analysis of Algorithms" lectures](https://www3.cs.stonybrook.edu/~skiena/373/videos/) by Steven S. Skiena

## Connectivity
- Single-pair connectivity:
  - Breadth First Search (BFS)
  - Depth First Search (DFS)
- Strongly connected components:
  - Tarjan's algorithm
  
## Traversal
- To-Do

## Topological sort
- Kahn's algorithm
- Depth First Search (DFS)

## Shortest path
- Single-pair shortest path problem:
  - A* search algorithm: heuristics to try to speed up the search.
- Single-source shortest path problem (equivalently, single-destination shortest path problem): 
  - Dijkstra's algorithm: non-negative edge weight
  - Bellman-Ford algorithm: edge weights may be negative
- All-pairs shortest path problem:
  - Floyd–Warshall algorithm
  - Johnson's algorithm: faster than Floyd-Warshall for sparse graphs
- Shortest stochastic path problem:
  - Viterbi algorithm

## Covering / Assignment
- [(Minimum cardinality) set cover](https://en.wikipedia.org/wiki/Set_cover_problem): [more](https://jeremykun.com/2015/05/04/the-many-faces-of-set-cover/)
- Minimum edge cover
- Hitting problem
- Perfect matching existence
- Maximum cardinality matching
- Maximum weight matching


# Optimization
## Learning
- [Lagrange multipliers](http://www.onmyphd.com/?p=lagrange.multipliers), simple mathematical/graphical justification of the Lagrange multipliers method
- [Karush-Kuhn-Tucker (KKT) conditions](http://www.onmyphd.com/?p=kkt.karush.kuhn.tucker), simple mathematical/graphical justification of the KKT conditions and how to deal with inequality constraints in an optimization problem

## Modelling languages
- [CVX (Matlab)](http://cvxr.com/cvx/), [CVXPY (Python)](http://www.cvxpy.org/en/latest/), [Convex.jl (Julia)](https://convexjl.readthedocs.io/en/latest/)
- [AMPL](https://ampl.com/)
- [YALMIP (Matlab)](https://yalmip.github.io/)
- [JuMP.jl](http://www.juliaopt.org/JuMP.jl/latest/)
- [Picos (Python)](http://picos.zib.de/index.html)
- [Google's OR-Tools](https://developers.google.com/optimization), optimization suite: constraint optimization, integer optimization, routing, network flow, assignment 

## Solvers
- [List of solvers for CVX](http://cvxr.com/cvx/doc/solver.html)
- [List of solvers for CVXPY](http://www.cvxpy.org/en/latest/tutorial/advanced/#choosing-a-solver)
- [List of solver in JuliaOpt](http://www.juliaopt.org/)
- [List of solvers for AMPL](https://ampl.com/products/solvers/all-solvers-for-ampl/)
- [List of solvers for YALMIP (by problem class)](https://yalmip.github.io/allsolvers/)
- [List of solvers for JuMP.jl](http://www.juliaopt.org/JuMP.jl/latest/installation.html#Getting-Solvers-1)
- Promising free solvers to try:
  - [OQSP](http://osqp.readthedocs.io/en/latest/) & [MIOQSP](https://github.com/oxfordcontrol/miosqp)
  - [Suggest-and-Improve framework for QCQPs](https://github.com/cvxgrp/qcqp)
  - Ipopt + [PyIpopt](https://github.com/xuy/pyipopt), smooth nonconvex program solver
  
## Tricks & problem conversions
- [MOSEK Modeling Cookbook](https://docs.mosek.com/modeling-cookbook/index.html)
- Specific tricks:
  - Removing integrality constraints: [linear program relaxation and integrality gap](https://en.wikipedia.org/wiki/Linear_programming_relaxation)
  - [Convex QCQP to SOCP](https://math.stackexchange.com/questions/1330896/can-a-convex-qcqp-with-an-additional-linear-constraint-be-converted-into-a-socp)
  - [Convex QCQP to SDP](https://mathoverflow.net/questions/58383/complexity-of-convex-quadratically-constrained-quadratic-programming-qcqp) 
  - [Least Absolute Deviations to LP](https://en.wikipedia.org/wiki/Least_absolute_deviations#Solving_using_linear_programming)
- [Iterative Reweighted Least Squares](https://cnx.org/contents/krkDdys0@12/Iterative-Reweighted-Least-Squares): solve minimization problems involving Lp-norms
  
