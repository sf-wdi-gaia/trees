# Breadth First

Breadth First Search is an algorithm for searching through graphs, looking for one or more nodes that meet some search criteria. Breadth first ordering can also be used to traverse a graph, that is, to visit all of its nodes.

When searching for a particular key in a binary search tree, we can take advantage of the fact that each node's left subtree contains smaller keys and each node's right subtree contains larger keys. Breadth First Search is more general -- it doesn't make any assumptions about the relationships among nodes' keys. In fact, we can search by criteria that aren't based on keys at all. 

**Breadth First Search chooses a start node and "visits" every node of a graph in order of how many edges the node is from that start.**  In a tree, we pick the root as the start node. We'll also consider each node to be the same "length." In graph terms, that means the "weight" of each edge is the same. Breadth first search only works for graphs with unweighted edges or graphs where all the edge weights are the same.

Breadth First Search spreads across the tree or graph like mold on bread, moving outward one step at a time from its start location.  The algorithm keeps track of which nodes to process with a queue, since it wants to process the nodes in the order it encountered them.  Pay attention to the order nodes are turning black in the animation below.   

<img src="https://upload.wikimedia.org/wikipedia/commons/4/46/Animated_BFS.gif" alt="breadth first search animation for tree" width="300px">

What's happening in that animation?   

```
node queue starts out with just root:
	[a]
enqueue first item's children; dequeue first item:
	[b, c]			=> a
enqueue first item's children; dequeue first item:
	[c, d, e]		=> b
enqueue first item's children; dequeue first item:
	[d, e, f, g]	=> c
enqueue first item's children (none!); dequeue first item:
	[e, f, g]		=> d
keep repeating until the queue is empty:
	[f, g, h]		=> e
	[g, h]			=> f
	[h]				=> g
	[]				=> h
```


## Exercises: Breadth First Tree Search

1. In English, describe how you would use breadth first search to find any node with a given key. Your algorithm should assume you have a tree data structure and that you can access each node's key and its array of children. (Do not assume it's a binary search tree.) You should also assume you're given a target key to match.

1. On the whiteboard, pseudocode a breadth first search function. Assume you have a tree data structure that allows the following operations:

	* given a tree/node `my_tree`, get the root of the tree with `my_tree`
	* given a tree/node, get the key of the node with `.key`
	* given a tree/node, get the children of the node with `.children`



1. Copy the starter code in either `tree.js` or `tree.rb`.  Code up your breadth first search function in one of these files. There are informal "tests" at the bottom of each file that show what the output should be.  Run `node tree.js` or `ruby tree.rb` to see these tests work on your file.



1. How would you modify your breadth first search function to work on a binary search tree?



1. Binary search trees can be faster than arrays at keeping data sorted when you insert and remove nodes, but only if the binary search tree is *balanced*, because a balanced tree has the minimum possible number of levels to store all its nodes. We can check that a tree is balanced by looking at where it has "missing children," room where nodes could have a child but don't. A tree is balanced if all of the missing children are at the very bottom level of the tree or just one level higher. How could you use breadth first search to check whether a binary search tree is balanced?



1. How could you modify breadth first search to pick out a group of nodes? What about selecting nodes based on some other characteristic instead of just the key?
