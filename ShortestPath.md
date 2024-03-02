# Introduction

I want to create a cheat sheet for shortest path algorithms. It should be better than what I created last time. If possible, I will try to add some code snippets as well. 

# Articles read

I will list down the articles that I am going through. 

- https://brilliant.org/wiki/shortest-path-algorithms/

# Summary

## Types of shortest path algo

1. Single source -> Find shortest path ebetween a single source and all other nodes. This can also work for single destination questions, by simply reversing the edges.

2. All Pairs -> The term is self explanatory. The most common algo here is Floyd Warshall

## Single source algo

### Bellman Ford

1. Edges can have -tive weights

2. Graph has to be directed. 

3. Bellman can detect -tive cycles


### Dijkstra's algorithm

1. Uses BFS

2. There can be no -tive weight edges

3. Its faster than Bellman Ford

### Topological Sort

1. Single source algo for DAG. 

2. Works in linear time

3. Can handle -tive edges and by definition will have no -tive cycle since DAG. 

## All source

### Floyd-Warshall algorithm

1. It uses DP
2. Can handle -tive cycle and -tive edges

### Johson's algorithm

1.  Floyd Warshall works well for dense graphs or graphs with many edges. Johnson works well for sparse graphs (few edges) .

# Comparison

![Algo comparisons](/screenshots/comparison.png)
