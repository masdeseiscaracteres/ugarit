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
