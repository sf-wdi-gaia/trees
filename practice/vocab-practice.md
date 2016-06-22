
## Vocab Practice

1. Use the diagram below to fill in the following table:


	| Node  | parent | left child | right child |
	| :---- | :-- | :-- | :-- |
	| A |  |   |  |
	| B |  |  |  |
	| C |  |   |   |

 <details><summary>click for solution</summary>
  
  | Node  | parent | left child | right child |
  | :---- | :-- | :-- | :-- |
  | A | *B* | *none*  | *none*  |
  | B | *D* | *A* | *C* |
  | C | *B* |  *none* |  *none* |
	
	</details>


  <img src="images/labels.jpg" width="300px">

1. In the same diagram (above), which node is the root?  Which are leaves?

  <details><summary>click for solution</summary>
  *D is the root.  A, C, and E are leaves.*
  </details>

1. Finally, in that same diagram, what is the height of the tree?

  <details><summary>click for solution</summary>
  *The height is 2, because the longest path from root to leaf has 2 edges/branches in it.*
  <br><br>
  </details>

1. Which of the following is a tree? (There may be more than one.)

  <img src="images/which_tree.jpg" width="300px">

  <details><summary>click for solution</summary>
  *B, D, E are trees.*

  *A is not a tree because one node has 2 parents.*

  *C is not a tree because there is a cycle (a circular path from one node back to that same node).*

  *F is not a tree because it's 2 trees! This is called a "forest".*

 </details>

1. Which of the following is a balanced tree? (There may be more than one.)

  <img src="images/which_balanced.jpg" width="300px">

  <details><summary>click for solution</summary>
  *B, D, and C are balanced because all of the "missing children" in these trees are either at the bottom level or one level above.*
  </details>

1. Which of the following is a binary search tree? (There may be more than one.)

  <img src="images/which_bst.jpg" width="300px">

  <details><summary>click for solution</summary>
  *Only the tree rooted with 6 is a binary search tree. The others both have nodes in the root's left subtree that are greater than the root node.*
  </details>
