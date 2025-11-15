# 8 November 2025

## Example Laying telephone wire


## Minimum spanning tree or Minimum cost spanning tree

- Connect all edges whose cost is minimum
- Its sub graph
- Its a tree `it is acyclic`
- It covers all Vertices
  - Contains |V| - 1 edges `This is in general tree property`
- The total with tree edges is the minimum cost
- It does not have a close boundary
- It does not allow disconnected vertices
- Multiple spanning tree but few MST with same weight
- Minimum edge will be always there
- Maximum edge in most of the cases will be avoided

> Can a graph have a MST ?
> A graph has a Minimum Spanning Tree if:
- It is connected: There is a path between every pair of vertices.
- It is undirected: MSTs are defined for undirected graphs.
- It has weighted edges: MST minimizes the total edge weight.

> MST Undirected Graph: 
> Single source shortest path problem Directed Graph
> All pair shortest path problem Directed Graph

## Kruskal's algorithm

- It is greedy algorithm `local minimum or benifit at first`
- Steps
  - Sort edges
  - Select edge `no loop with minimum cost`
  - Repeat untill all verices are connected

> When a graph has multiple edges with same weight then possibly it has more than one MST
> 

## Prim's algorithm

- Where we have to start this is given if source is not given then select node with `highest inorder`
- Pick minimum edge and `mark it as visited`
- Choose connected Vertices `with least weight` from the source node
- Repeat untill V-1 edges
- Edge weight is considered

> Prim's and Krushal algorithm uses undirected graph