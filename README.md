# Trees: Quick Reference

#### Graph


<img src="images/graph-terms.png" width="350px">

* stores data in vertices (also called nodes)
* vertices are connected by edges, which represent relationships or transitions
* edges can be undirected (two-way) or directed (one-way)
* each node usually has a key and often some extra associated data we care about

Operations for a graph:
* given a vertex, find all *adjacent* vertices (nodes it's connected to by an edge)
* given an edge, find the two nodes it connects (and know which is the start node, if the edge is directed)

Uses of graphs:
 * flow charts
 * route planning
 * goal-seeking artificial intelligence

<hr>

#### Tree

<img src="images/tree-terms.png" width="300px">

* type of graph
* rooted (has a single start point)
* edges/branches usually directed (one-way), away from the root
* doesn't allow cycles, or circular paths ("acyclic")
* each node can have only one parent, so only one branch can lead into it
* time for many operations is related to the *height*


Operations for a tree:
  * access the root node  
  * get the key of a given node
  * get an array of all the nodes that are children of a given node

Uses of trees:
  * modeling decision-making processes over time
  * representing hierarchies like a company's direct reporting structure
  * keeping track of data that is too large to fit in one chunk in a computer's memory (like most files)

<hr>

#### Binary Search Tree
**very common in interviews**

<img src="images/bst-example.png" width="300px">

* kind of tree
* max number of children per node: 2 (this makes it a "binary" tree)
* stores data in an easily sorted order (keys have to be sortable)
* binary search tree property:  
  * left subtree of any node has all keys less than or equal to the node's key (*If it's less, it's to the left!*)  
  * right subtree of any node has all keys greater than or equal to the node's key  
* height with `n` nodes:
  * if balanced, `O(log(n))`  
  * if not balanced, `O(n)`

*A balanced binary search tree is as short as it can be - it has "missing children" only on its bottom level and the level right above the bottom. We care because shorter trees are faster, so <strong>balanced</strong> binary search trees are faster than unbalanced!*

Operations for a binary search tree:
  * access the root node
  * get the key of a given node
  * get the right child node of a given node (or `None` if there isn't one!)
  * get the left child node of a given node (or `None` if there isn't one)

Uses of binary search trees:
  * storing sorted data

<hr>

#### Trie

<img src="images/trie-example.png" width="400px" alt="trie storing on, one, tan, tap, tar, two">

*on, one, tan, tap, tar, two*

* kind of tree
* stores sequential data
* each node adds to the sequence
* nodes that are the end of a word or sequence are marked
* height not determined by number of nodes


Operations for a trie:
  * access the root node
  * given any node, get its key
  * given any node, get a boolean that will be true if the node is the end of a word
  * given any node, get an array of all the nodes that are its children

Uses of tries:
  * autocomplete
  * spell checking
