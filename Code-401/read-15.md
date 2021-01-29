# Notes for Read 15 - Trees

[Code Fellows - Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

Critical terms for Trees
+ Node
+ Root
+ Left Child
+ Right Child
+ Edge
+ Leaf
+ Height

Can traverse a tree in two ways:
+ Depth - Search down each branch
+ Breadth - search across the levels of the tree

For Depth First Three ways to traverse it:

PreOrder -> Start at root, check left, check right.
In-Order -> Check left, root, then right.
Post-Order -> Check left, right, root

Breadth First

Use a Queue with recursion.
Starts with root.  Enqueues left and right nodes

Binary Trees are organized in such a way that values greater than the root are on the right and vice-versa for left.

BigO

Space: O(1)
Time: O(logN) balance O(n) unbalanced







[&lt;--&#91;BACK&#93;](/README.md)