# 11 October 2025

> [Linked from previous session on 5-October-2025](https://github.com/Sombaran/mtechDocumentsSlides/blob/main/SEM_1/ECS5101/5OctSess.md)
> [Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/cs514cse_iitp_ac_in/Documents/Recordings/ECS%205101%20Lecture%20Room-20251011_080514-Meeting%20Recording.mp4?csf=1&web=1&e=1vjOWg&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)


## Deletion of BST Node

- Deletion uses `FIND algorithm` to find location of the node data and location of the `Parent Node`
- 3 Cases
  - No child
  - One child: either left or right
  - Two child: then delete node after taking `InOder successor` node 


## Drawback of BST

- In BST we hold a property of `Left < Root < Right` but consider an example:
  - 46 48 55 66 81 91 100 105 144: Here `Root < Right` which is fullfiling all property of BST but this example is similar to linear array with complete of `O(N)` which is voilation of `O (log2N)`
- If tree is left skwed or right skwed then complexity of BST changes from  `O (log2N)` to `O(N)` making tree unbalanced and voilation from BST property

## AVL Tree Adelson - Veleskii - Landis 

- AVL Tree is `balanced BST`
- It balances the left and right height and ensures `balance factor`of all the node is either `0/1/-1`
- It is specialized balanced tree where `balance factor`of all the node is either `0/1/-1`
- An empty binary tree is an AVL tree
- What is balance factor?
  - Difference between left height and right height
- If balance factor is `0/1/-1` then then BST is an `AVL Tree` is a fairly balanced tree

> While doing insertion and deletion balance factor gets effected and then we need to perform rotations to achieve desirable balance factor.

## Rotation in AVL tree

- LL
  - Uses single rotation
  - Identify the first node `A` from point of insertion that is violating AVL Tree property
  - Make that node `A` and its left child `B`
  - `B` goes up and `A` comes down and `B` right child becomes `A` left child
- RR
  - Uses single rotation
  - Identify the first node `A` from point of insertion that is violating AVL Tree property
  - Make that node `A` and its right child `B`
  - `B` goes up and `A` comes down and `B` left child becomes `A` right child
> `LL and RR` are also called as `mirror imaging rotations`
- LR
  - Uses two 2 rotations
  - First Rotation is RR and then LL
- RL
  - Uses two 2 rotations
  - First rotation is LL and then RR
