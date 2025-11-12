# 4 October 2025 

> All trees are graphs are but all graphs are not trees
> [Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/cs514cse_iitp_ac_in/Documents/Recordings/ECS%205101%20Lecture%20Room-20251004_081311-Meeting%20Recording.mp4?csf=1&web=1&e=bmJtLh&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)


## Tree data structure

- Sequence of access elements in hierarical thats why it is called non-linear data structure.
- Loop is not formed here becuase closed boundary is formed and it becomes a graph
- Trees are special form of graph that does not form cyclic form of nodes
- Trees are subset of graph with a condition of not having loop

## Binary Tree

- Represented by T 
- T empty called as _null or empty tree_ 
- Node with no child is called _terminal node_ / _leaf node_
- A Binary tree can have only 0/1/2 child
- starting is a root node
- All subtree in a tree is also a _tree_
- Copies does not mean same number of node but it means _same arrangement of node_

## Why trees are so important (Binary tree)

- Ultimate aim of any processor/ computing system is to perform mathematical expression
- Operator must be _root node_ and operand must be _child node_ 
- Starting node is called _root node_
- Root has _left child and right child_/ _left successor or right successor_/ _left descendent or right descendent_
- There is only _one root_
- _left child and right child_ is called _sibling_ and must be on _same level_
- _Two vertices_ are joined _edges_, _A_ to _B_ where A and B are called _vertices_
- Path Start from _A_ and go to _B_ and then to _C_ and node should be connected
- level: Root must at _0_ level, as we do down level increases
- Height of tree (Depth) is the maximum number of nodes in any branch of _T_
- Edge is the line joining `two nodes` or Two vertices are joined by one `Edge`

## Complete Binary Tree

- If all the nodes having _maximum_ possible child other than _leaf_ or _terminal node_ then it is called as _complete bianry tree_
- We try to accomodate all the nodes with maximum number of child
- If at last level it is not possible to accomodate child then we put at the _left node_ (__last && left node__)
- [Refer this link](https://www.geeksforgeeks.org/dsa/difference-between-full-and-complete-binary-tree/)

## Accessing in Tree

- Depth of tree = __log n + 1__
  - If n (nodes is 100000) then depth is 21

## Extended BT

- Also called 2-Tree
- If a node has 0 or 2 leaf node no node with 2 child is allowed
- Internal Node `Circle` and added node or external node `Square`

## Representation of Tree
    
- Sequential representation using single array
  - K and 2K+1
  - elimate space
  - depth needed will be `2^(d+1) elements`
- Linked representation using doubly linked list
  - 
## Traveral in Binary Tree

- Pre order   `Root Left Right`
- In order    `Left Root Right`
- Post order  `Left Right Root`

## Lab Exercise

[Click here for hackerrank link](https://www.hackerrank.com/contests/executive-m-tech-test-9/challenges)


