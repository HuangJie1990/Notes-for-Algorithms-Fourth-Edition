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

Insertion into a 3-node at bottom.

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

###### Key property. 1-1 correspondence between 2-3 and LLBB.



