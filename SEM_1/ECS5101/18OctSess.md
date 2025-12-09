## Lecture 16 October 18, 2025

- M-Way tree does not allow duplicate entry
- Before insertion or deletion we need to search the element and this seach has to happen to the depth of the tree
- M-way is not a height balancing tree
- Insertion is not performed on raw tree, it is the tree where number of operations has already happened.
- Lets make a m-way tree from scratch

> List 46 13 23 53 45 49 76 98 120 140 153 198 lets make 3-way tree;
3-way tree will have 2 keys and Adress/ child will be tree
Tree will either left or right skewed and hence it will break property of voilation of time complexity, therefore to balance this we have another tree called `balance m-way tree`

- Deletion 4 cases:
> if (Ai == Aj == nullptr) --> delete k
 
> else if ( Ai != nullptr && Aj == nullptr) replace Key with largest root element pointed by pointer

> else if ( Ai == nullptr && Aj != nullptr) replace Key with smallest root element pointed by pointer

> else if (Ai != nullpte && Aj != nullptr) choose any key to delete


## B-tree (Balanced M-way tree)

- M-way has an advantage of minimal file access due to its restricted height, however it is important to keep the height as low as possible and therefore there arise a need to balance m-way search tree and its is called as B-tree
## Properties of B-tree

- A B-tree of order m, if non-empty is an m-way search tree where:
- the root has `atleast 2 child and utmost m child`
- the internal node accept root have `atleast m/2 child nodes and utmost m child nodes`
- key 1 less than order
- all leaf nodes must be on same level

> Lets say m=3 then it is called 2-3 tree meaning 2 key 3 child as internal nodes can be of only degree 2 or 3 only

> Let say m=5 then it is called as 4-5 tree meaning

- Searching/ Traversal is similar to m-way tree
-  