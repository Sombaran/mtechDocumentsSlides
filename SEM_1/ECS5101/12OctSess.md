# 12 October session

> [Linked from previous session on 5-October-2025](https://github.com/Sombaran/mtechDocumentsSlides/blob/main/SEM_1/ECS5101/11OctSess.md)
> [Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/cs514cse_iitp_ac_in/Documents/Recordings/ECS%205101%20Lecture%20Room-20251012_080430-Meeting%20Recording.mp4?csf=1&web=1&e=tAY0zH&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)

## Rotation in AVL tree

- LL
  - Uses single rotation also called with notation as `R-0` doing `Single Right Rotation`
  - Identify the first node `A` from point of insertion that is violating AVL Tree property
  - Mark that node `A` and its left child `B`
  - `B` goes up and `A` comes down and `B` right child becomes `A` left child
- RR
  - Uses single rotation also called with notation as `R-3` doing `Single Left Rotation`
  - Identify the first node `A` from point of insertion that is violating AVL Tree property
  - Mark that node `A` and its right child `B`
  - `B` goes up and `A` comes down and `B` left child becomes `A` right child
> `LL and RR` are also called as `mirror imaging rotations`
- LR
  - Uses two 2 rotations also called with notation as `R-1` doing `Double Rotation: Left then Right`
  - First Rotation is RR and then LL
- RL
  - Uses two 2 rotations also called with notation as `R-2` doing `Double Rotation: Right then Left`
  - First rotation is LL and then RR

> Time complexity in AVL Tree is O(height) =  O(log N)

## M-way tree
