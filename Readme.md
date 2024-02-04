# Introduction

One place to document well known graph theory concepts. I might extend this repository to other data structures as well. This repo will mostly focus on theory, and not on actual code, unless its needed to understand the theory.

## Shortest Path finding algorithm (Single Source)

### Dijkstra's Algorithm

**Limitations**
1. Does not work with -tive edges.
2. It has to have a single source. So you can determine the shortest path from a single source.
3. Can be slower than algorithms like A* if a good heuristic is available.
4. Only tells you the shortest path, not how much faster it is compared to other possible paths.

**Facts**
1. Works for both directed and indirected 
2. Can also handle cycles
------------
### Bellman-Ford Algorithm

**Limitations**
1. When there are negative-weighted edges in the graph, because then Dijkstra isn't guaranteed to work. Not only will Bellman-Ford not break for negative-weighted edges, it will also tell you (at least you can derive that information from it) if there is a negative-weighted cycle in the graph
2. Bellman-Ford is also a single source shortest path algorith
3. Slower than Dijkstra's for non-negative weights: Not the best choice if your graph doesn't have negative edges.
Can't handle negative cycles: If your graph has a cycle with a total negative weight, it will loop infinitely without finding any paths.
4. Can't handle negative cycles: If your graph has a cycle with a total negative weight, it will loop infinitely without finding any paths.

**Facts**
1. Works for both directed and indirected graph.
2. Can also handle cycles

### A Search Algorithm:* 

Uses heuristics to guide the search and often finds the shortest path faster than Dijkstra's, especially for graphs with good heuristics.

**Limitations**
1. Reliance on heuristics: The performance heavily depends on the quality of the chosen heuristic. A bad heuristic can lead to significantly slower results or even failure to find the optimal path.

## All Pairs Shortest Path (APSP):

### Floyd-Warshall Algorithm

Computes the shortest paths between all pairs of nodes in a weighted graph with non-negative edge weights. This is a dynamic programming approach and guarantees finding all shortest paths, but can be memory-intensive for large graphs.
It works for both directed and undirected

**Limitations**
1. High memory usage: Can be computationally expensive for large graphs due to storing all-pairs shortest paths.
2. Not suitable for dynamic graphs: If your graph changes frequently, finding all-pairs shortest paths every time might be inefficient.
3. Redundant computations: Many shortest paths might already be known from previous computations, but the algorithm recalculates them anyway.
4. Does not work for graphs with -tive cycle

### Johnson's Algorithm:

Combines Dijkstra's algorithm with Bellman-Ford to find APSP in sparse graphs with positive, negative, but no negative cycle edge weights. This can be faster than Floyd-Warshall for certain graphs.

**Limitations**
1. More complex than Dijkstra's and Bellman-Ford: Requires combining and running both algorithms, adding additional steps and potential complexity.
2. Not always faster than Floyd-Warshall: For dense graphs, Floyd-Warshall might be faster due to its parallel calculations.

