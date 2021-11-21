# Construct-BST-from-given-preorder-traversal
Problem Statement : Given preorder traversal of a binary search tree, construct the BST.
Example :  if the given traversal is {10, 5, 1, 7, 40, 50}, then the output should be the root of the following tree.
     10
   /   \
  5     40
 /  \      \
1    7      50
Algorithm : The trick is to set a range {min .. max} for every node. Initialize the range as {INT_MIN .. INT_MAX}. The first node will definitely be in range, so create a root node. To construct the left subtree, set the range as {INT_MIN …root->data}. If a value is in the range {INT_MIN .. root->data}, the values are part of the left subtree. To construct the right subtree, set the range as {root->data..max .. INT_MAX}. 
