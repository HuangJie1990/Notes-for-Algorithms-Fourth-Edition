# 2-3 tree

##### Allow 1 or 2 keys per node.

* 2-node: one key, two children.
* 3-node: two keys, three children.

##### Sysmetric order.

Inorder traversal yields keys in ascending order.

##### Perfect balance

Every path from root to null link has same length.

##### Search.

* Compare search key against keys in node.
* Find interval containing search key.
* Follow assciated link \(recursively\).

##### Insertion into a 3-node at bottom.

* Add new key to 3-node to create temporary 4-node.
* Move middle key in 4 node int parent.
* Repeat up the tree, as necessary.
* If you reach the root and it's a 4-node, split it into three 2-nodes.

# red-black BSTs

##### Left-leaning red-black BSTs

1. Represent 2-3 tree as a BST.
2. Use "internal" left-leaning links as "glue" for 3-nodes.

##### An equivalent defination

A BST such thar:

* No node has two red links connected to it.
* Every path from root to null link has the same number of black links.
* Red links lean left.

###### Key property.

1-1 correspondence between 2-3 and LLBB.

###### Observation.

Search is the same as for elementary BST \(ignore color\). Most other ops \(e.g., floor, iteration, selection\) are also identical.

###### Left rotation.Invariants.

Orient a \(temporarily\) right-leaning red link to lean left. Maintains symmetric order and perfect black balance.

###### Right rotation.Invariants.

Orient a left-leaning red link to \(temporarily\) lean right. Maintains symmetric order and perfect black balance.

###### Color filp. Invariants.

Recolor to split a \(temporary\) 4-node. Maintains symmetric order and perfect black balance.

#### Insertion in a LLRB tree: overview

###### Basic strategy.

Maintain 1-1 correspondence with 2-3 trees by applying elementary red-black BST operations.

###### Warmup 1.

Insert into a tree with exactly 1 node.

Case 1. Insert into a 2-node at the bottom.

* Do standard BST insert; color new link red.
* If new red link is right link, rotate left.

总结：Case 1情况包括Warmup1情况。总是用红链接将新结点和它的父结点相连。如果只想新结点的是父结点的左链接（新结点比父结点小），那么父结点就直接成为一个3-结点；如果指向新结点的是父结点的右链接，这就是一个错误的3-结点，但一次坐旋转就能修正它。

###### Warmup 2. Insert into a tree with exactly 2 nodes.

Case 2. Insert into a 3-node at the bottom.

这种情况可以分成三种子情况：新键小于树中的两个键，在两者之间，或者大于树中的两个键，每种情况都会产生一个连接到两条红链接的结点。

总结：

* Do standard BST insert; color new link red.
* Rotate to balance the 4-node \(if needed\).
* Flip colors to pass red link up one level.
* Rotate to make lean left \(if needed\).
* Repeat case 1 or case 2 up the tree \(if needed\).

###### Same code for all cases.

* Right child red, left child black: rotate left.
* Left child, left-left grandchild red: rotate right.
* Both children red: flip colors.





