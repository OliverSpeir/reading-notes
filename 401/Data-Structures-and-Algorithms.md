# Data Structures and Algorithms
- Fundamental principles in computer science
- Problem Solving in the modern world is like standing on the shoulders of giants and there are many invaluable resources that reflect hours of work that one would be at a disadvantage without

## Content
- [Basic Recursion](https://www.youtube.com/watch?v=vPEJSJMg4jY)
- [Data Structures in 7 Minutes](https://www.youtube.com/watch?v=sVxBVvlnJsM)
- [Big O Explained](https://www.youtube.com/watch?v=v4cd1O4zkGw)
- [Basic Data Structures](https://towardsdatascience.com/8-common-data-structures-every-programmer-must-know-171acf6a1a42)
- [Why Big O](https://triplebyte.com/blog/why-you-should-learn-big-o-and-stop-hacking-your-way-through-algorithms)

## Discussion Questions
### What is 1 of the more important things you should consider when deciding which data structure is best suited to solve a particular problem?
- How will the data be used and how will it need to be manipulated and how much data will there be? 

### How can we ensure that we’ll avoid an infinite recursive call stack?
- Having a Base Case aka having the function exit itself or a plan to consider what will stop it under all possible circumstances

## Content Notes

### [Basic Recursion](https://www.youtube.com/watch?v=vPEJSJMg4jY)
- Base Case and Recursive Case
- Pseudocode = high level description written in human language 
- While loops can often be used but are bulky
- <img src="https://i.imgur.com/OTgLIlB.png"/>
- Recursion usually isn't faster and sometimes is slower, but it looks cleaner and easier to understand
- Base Case is when function doesn't call itself
- Recursive Case is when function calls itself

### [Data Structures in 7 Minutes](https://www.youtube.com/watch?v=sVxBVvlnJsM)
- Compound Data is a collection of data items
- Big O notation is how effective a data structure is
- List of top 5 Data Structures
1. Linked List 
 - Each unit of a linked list is called a Node
 - Node contains value and pointer
 - First node is head
 - last is tail
 - Pro: Good at adding and deleting nodes
 - Con: Not good at retrieval or searching
2. Array
 - Continuous block of cells in computer memory, memory location is kept track of which allows any cell to be accessed from anywhere
 - Pro: Retrieval 
 - Con: Adding items (mostly for lower level languages)
3. Hash Table
 - Object in JS or Dictionary in Py
 - Works like array in terms of memory location but they aren't in continous block 
 - Pro: add and remove
 - Con: Collision (two keys hasing to same memory location)
4. Stack and Queue
 - Stack is last in first out data structure (push and pop off top)
 - Stack is for DFS (depth first search)
 - Queue is a line and is first in first out (enqueue and dequeue)
 - Queue is for BFS (breadth first search)
 - Pro: Efficient add and remove
 - Con: Limited use cases
5. Graphs and Trees
 - Graph theory
 - Each unit is a node with a value and pointers
 - pointers are called edges and can have weights assigned to them
 - edges can be thought of like roads between cities, the road is the edge and the weight is the length of the road
 - Tree is a hierarchical graph where edges branch out in one direction
 - Binary Search Tree has specific rules: Each node can only have 0-2 children (left and right), left has to be less than node and right has to be more (these trees can become unbalanced)
 
### [Big O Explained](https://www.youtube.com/watch?v=v4cd1O4zkGw)
- Big O aka algorthimic effeciency 
- Story of Carrier pigeon with a USB versus a big file over slow internet 
- Big O calls the pigeon or constant time O(1)
- Internet transfer time is O(n) (scales linearly with amount of data)
- If you have two steps you add them aka step 1 is O(a) and step 2 is O(b) so whole function is O(a+b)
- If you have two constants in Big O you drop them, so if Step 1 is O(a) and step 2 is O(a) you do not say whole function is O(2a) it is just O(a)
- If function searchs two different arrays it is not O(n^2) it is O(a * b)
- If you have a non dominate term you do not include it if function step 1 is O(n) and step 2 is O(n^2) you do not call it O(n+n^2) it is just O(n^2)
### [Basic Data Structures](https://towardsdatascience.com/8-common-data-structures-every-programmer-must-know-171acf6a1a42)
- Currently pay-walled on Medium (will update)
### [Why Big O](https://triplebyte.com/blog/why-you-should-learn-big-o-and-stop-hacking-your-way-through-algorithms)
- [Big O Cheat Sheet](https://www.bigocheatsheet.com/)
- [Math Speak](https://triplebyte.com/blog/confused-by-algorithms-introducing-math-speak-the-secret-language-nobody-told-you-about)
- Big O is worth learning because it will help understanding of algortihms in general and is not as intimidating as it seems
- Big O is just a notation 
- Effeciency is everything with algorithms and missing that point makes everything more confusing
- Making log time is cutting half the possible options at each decision point
- Making log time is the point of using BST which makes BST make sense (BST being a tree that you either go left or right in to find your answer)
- Learn all agorithms in parallel with their effects on time and space 
- " “the time complexity of this function is O(n).” The letter “O” can just be thought of as shorthand for the rough “order” of magnitude of operations it takes to run the function, while “n” represents the possible number of vegetables passed in each time. So O(n) is just a math-style way of describing roughly how long (in the worst case) a function will take in terms of the number of inputs passed in. Easy peasy."


