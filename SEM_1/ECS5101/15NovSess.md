# 15 November 2025

## Single source shortest path

- GPS mapping 
- In Kruskal and prim's algorithm 
- Edge and vertex weight we need to consider
- Steps
    - Initialize single source on each vertex and other as infinity
    - Edge + vertex weight
    - Relax
    - Negative and negative edge cycle

## Variants in SSSP

- Single destination shortest path problem `Prim's`
- Single-pair shortest path problem `Bellman Ford && Dijkstra`
- All pair shortest path problem `Flyord worshall`
> Bellman Ford allows negative edge 
> Dijkastra allows edge ngative 
> Sub path of shortest path are shortest path 
                NegativeE   NegativeECycle
Bellman         ok          Nok
Dijkastra       Nok         Nok
Worshall        ok          Nok

> Why negative edge cycle is not allowed by any algorithm? --> Infinity cycle

## Bellman Ford

- Return boolean
- If false: stuck in infinite loop
- 
