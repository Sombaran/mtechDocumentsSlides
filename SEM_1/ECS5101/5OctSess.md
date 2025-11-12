# 5 October 2025

> [Linked from previous session on 4-October-2025](https://github.com/Sombaran/mtechDocumentsSlides/blob/main/SEM_1/ECS5101/4OctSess.md)
> [Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/cs514cse_iitp_ac_in/Documents/Recordings/ECS%205101%20Lecture%20Room-20251005_080514-Meeting%20Recording.mp4?csf=1&web=1&e=JQYJ6G&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D) 
## Traversal in Binary Tree

- PreOrder
```C++
    void PreOrderBSTTraversal(PreOrderBST *obj) {
        if (obj == nullptr) {
            return;
        }
        std::cout << obj -> mData << " ";
        PreOrderBSTTraversal(obj -> mLeft);
        PreOrderBSTTraversal(obj -> mRight);
    }
```
- InOrder
```C++
    void InOrderTreeTraversal(InOrderTree *obj) {
        if (obj == nullptr) {
            return;
        }
        InOrderTreeTraversal(obj -> mLeft);
        std::cout << obj -> mData << " ";
        InOrderTreeTraversal(obj -> mRight);
    }
```
- PostOrder
```C++
    void PostOrderBSTTraversal(PostOrderBST *obj) {
        if (obj == nullptr) {
            return;
        }
        PostOrderBSTTraversal(obj -> mLeft);
        PostOrderBSTTraversal(obj -> mRight);
        std::cout << obj -> mData << " ";
    }
```

## Tree reconstruction

- We need to 2-Traversal to reconstruct the tree
- PreOder and InOrder
- Steps
  - Pick a node from `PreOrder from start which is root` and indentify its position on the Inoder and then decide left and right
  - Pick a node from `PostOrder from end which is root` and indentify its position on the Inoder and then decide left and right
  - If node is marked is already covered then we cannot accomodate to the tree

## Binary search tree or Binary Sorted Tree

- One of the most important DS in computer science because it uses `O(log2 n)` for searching, deletion and search.
- Application: Used to remove duplicate elements.
- This complexity match with linear array `binary search` and `linear linked list`.

## Properties of BST

- Left child value is less than root and further lesser than right `Left < Root < Right`.
- Never allow duplicate element.
- While doing `search and traversal` the above 2 properties are not effected but it might get affected during `insertion and deletion`. Therefore while doing `insertion and deletion` we need to restore back the property of the tree.
- Entry point is root.
- BST is popular as it computational complexity is in `O log 2 N` for searching, insertion and deletion.
- Number of comparisons in BST is bounded by the `depth of the tree` and this comes from the fact that we proceed down a single path of the tree.
- The running time is directly proportional to the depth of the tree.
- All BST are generally a `Complete binary tree` but all `Complete binary tree` are not `BST`

## Insertion in BST

```C++
    PostOrderBST* insertIntoBST(PostOrderBST *obj, int val) {
    /**
    Construct a sample binary tree
            10
           /  \
          5    15
         / \   / \
        2   7 12  17
    */
    
        if (obj == nullptr) {
            return new PostOrderBST(val);
        }
        if (val < obj -> mData) {
            obj -> mLeft = insertIntoBST(obj -> mLeft, val);
        }
        else 
        {
            obj -> mRight = insertIntoBST(obj -> mRight, val);
        }
        return obj;
    }
```
- It is second phase of searching.
  - First search the particular node and if it is not found then insert it


## Deletion in BST

- Deletion uses `FIND algorithm` to find location of the node data and location of the `Parent Node`
- 3 Cases
  - No child
  - One child: either left or right
  - Two child: then new take delete node after taking `InOder Traversal`