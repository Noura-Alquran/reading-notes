# Read: Trees Summary:
## Common Terminology
1. **Node** - A Tree node is a component which may contain it’s own values, and references to other nodes
2. **Root** - The root is the node at the beginning of the tree.
3. **K**- A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
4. **Left** - A reference to one child node, in a binary tree
5. **Right** - A reference to the other child node, in a binary tree
6. **Edge** - The edge in a tree is the link between a parent and child node
7. **Leaf** - A leaf is a node that does not have any children
8. **Height** - The height of a tree is the number of edges from the root to the furthest leaf.

## Traversals:
* Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! 
* There are two categories of traversals when it comes to trees:
  1. **Depth First** : is where we prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes the order in which we search/print the root. Here are three methods for depth first traversal:
    + Pre-order: root >> left >> right
    + In-order: left >> root >> right
    + Post-order: left >> right >> root
  2. **Breadth First** : iterates through the tree by going through each level of the tree node-by-node.
    + Traditionally, breadth first traversal uses a **queue** (instead of the call stack via recursion) to traverse the width/breadth of the tree. 
## Binary Tree Vs K-ary Trees
* Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).
## Big O:
* The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height). In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.
* The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.

## Binary Search Trees
* A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.
