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

Case 1. 

Insert into a 2-node at the bottom.

* Do standard BST insert; color new link red.
* If new red link is right link, rotate left.







