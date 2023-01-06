# Trees

## Resources

- [Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

### Common Terms

- Node - A Tree node is a component which may contain its own values, and references to other nodes
- Root - The root is the node at the beginning of the tree
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left - A reference to one child node, in a binary tree
- Right - A reference to the other child node, in a binary tree
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not have any children
- Height - The height of a tree is the number of edges from the root to the furthest leaf

<img src ="https://i.imgur.com/QsxBnP6.png"/>

### Traversal

- Depth First
- Breadth First


#### Depth First

- Depth first traversal is where we prioritize going through the depth (height) of the tree first.
- Using recursion and call stack


- Pre-order: root >> left >> right
- In-order: left >> root >> right
- Post-order: left >> right >> root

``` pseudo
ALGORITHM preOrder(root)

  OUTPUT <-- root.value

  if root.left is not NULL
      preOrder(root.left)

  if root.right is not NULL
      preOrder(root.right)
```

``` pseudo
ALGORITHM inOrder(root)
// INPUT <-- root node
// OUTPUT <-- in-order output of tree node's values

    if root.left is not NULL
        inOrder(root.left)

    OUTPUT <-- root.value

    if root.right is not NULL
        inOrder(root.right)
```
``` pseudo
ALGORITHM postOrder(root)
// INPUT <-- root node
// OUTPUT <-- post-order output of tree node's values

    if root.left is not NULL
        postOrder(root.left)

    if root.right is not NULL
        postOrder(root.right)

    OUTPUT <-- root.value
```

#### Breadth First

- Traditionally, breadth first traversal uses a queue (instead of the call stack via recursion) to traverse the width/breadth of the tree.
- enqueue left child node first then right 
  - dequeue after enqueuing all child nodes

``` pseudo
ALGORITHM breadthFirst(root)
// INPUT  <-- root node
// OUTPUT <-- front node of queue to console

  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while ! breadth.is_empty()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    if front.left is not NULL
      breadth.enqueue(front.left)

    if front.right is not NULL
      breadth.enqueue(front.right)
```

#### K-ary Trees

- can have K number of child nodes, as opposed to binary which can only have 2 children nodes

- Traversing a K-ary tree requires a similar approach to the breadth first traversal. 
  - We are still pushing nodes into a queue, but we are now moving down a list of children of length k
    - instead of checking for the presence of a left and a right child.

```pseudo
ALGORITHM breadthFirst(root)
// INPUT  <-- root node
// OUTPUT <-- front node of queue to console

  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while ! breadth.is_empty()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    for child in front.children
        breadth.enqueue(child)
```


#### Adding Nodes

- Not neccesarily rules for where nodes are "supposed to go"

- One strategy highlighted is to use BFT and find the first node where there is only 1 child

#### Big O 

- Big O for time is O(n) due to traversing 

- Big O for space is O(w) where w is width of tree

#### Binary Search Trees

- A Binary Search Tree (BST) is a type of tree that does have some structure attached to it

- All values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right

- Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree.
  - If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side

- He best way to approach a BST search is with a while loop

  - We cycle through the while loop until we hit a leaf, or until we reach a match with what we’re searching for


- BIG O for time is O(H) where H is height
  - balanced (or “perfect”) tree, the height of the tree is log(n)
  - if unbalanced h is n
- BIG O for space is O(1) as no extra memory is allocated 