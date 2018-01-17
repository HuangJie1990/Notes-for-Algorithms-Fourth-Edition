# BSTs

**Definition**. A BST is a binary tree in symmetric order.

A binary tree is either:

* Empty.
* Two disjoint binary trees \(left and right\).

**Symmetric order**.

Each node has a key, and every node's key is:

* Larger than all keys in its left subtree.
* Smaller than all key in ites right subtree.

**Search**. If less, go left; if greater, go right; if equals, search hit.

**Insert**. If less, go left; if greater, go right; if null, insert.

**Get**. Return value corresponding to given key, or null if no such key. **Cost**. Number of compares is equal to 1 + depth of node.

**Put**. Associate value with key. **Cost**. Number of compares is equal to 1 + depth of node.

Search for key, then two cases:

* Key in tree =&gt; reset value.
* Key not in tree =&gt; add new node.

## Hibbard deletion

To delete a node with key k: search for node t containing key k.

Case 0: \[0 children\] Delete t by setting parent link to null.

Case 1: \[1 childern\] Delete t by replacing parent link.

Case 2: \[2 childern\]

* Find successor x of t. x has no left child.
* Delete the minimun in t's right subteree.
* Put x in t's spot.



