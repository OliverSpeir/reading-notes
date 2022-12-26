# Linked Lists
- Common fundamental data structure 
- [LinkedLists Part1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)
- [LinkedLists Part2](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)
- [Linked List Video](https://www.youtube.com/watch?v=lC-yYCOnN8Q)
- [Texas A&M LinkedList Document](https://people.engr.tamu.edu/j-welch/teaching/211.s03/lnotes1.pdf)
- [Beginners Guide to Big O by Rob Bell](https://robbell.io/2009/06/a-beginners-guide-to-big-o-notation)
- [BigO Cheat Sheet](https://www.bigocheatsheet.com)
- [StackOverFlow Array Vs Linked List](https://stackoverflow.com/questions/393556/when-to-use-a-linked-list-over-an-array-array-list)
- 


## Define 
- A linked List is a sequence of nodes that are connected to eachother. The most definining feature of a linked list is that each node refences the next node in the link
- Sinlgy and Doubly 

## Terminology
- Linked List: Data structure that contains nodes that link/points to the next node in the list
- Singly: Only 1 "reference/pointer/link" which is the the **next** node 
- Doubly: Two "references/pointers/links" which point the **next** node and **previous** node
- Node: Individual item of a list, contains the data for the item and the "link" itself 
- Next: Each node has property **next** which contains the reference to the next node
- Head: 1st node in the list
- Current: current node in the list, when traversing current variable is created at head in the beginning to keep track correctly 

## Visualization
<img src="https://i.imgur.com/XlJMHHx.png"/>

## Traversing
- Can't use for loops, need to use Next value to find position 
- Best method is while loop, allows to check next node until there is no next value 
    - NullReferenceException can come up when trying to traverse to null node
``` pseudo 
ALGORITHM Includes (value)
// INPUT <-- integer value
// OUTPUT <-- boolean

  Current <-- Head

  WHILE Current is not NULL
    IF Current.Value is equal to value
      return TRUE

    Current <-- Current.Next

  return FALSE
  ```
## Step through
1. Create Current at Head (guarantee we are at beginning)
2. while loop 
3. condition (value we are searching for is found)
4. when current does not satisfy the condition we move to the next and check condition 
5. repeat 3 + 4 until condition is met 
6. return false if value is not in list 

## Big O for Traverse 
- Includes (is value in list) is O(n) for time
- Includes is O(1) for space because no additional space is used

## Adding Node
- Order of Operations is very important
- all references must be properly assigned
- Need to replace the Head when you add a new node, but you cannot lose your position in the list
``` pseudo 
ALGORITHM Add(newValue)
// INPUT <-- Value to add
// OUTPUT <-- No output

  newNode <-- NEW Node
  newNode.Value <-- newValue
  newNode.Next <-- Head
  Head <-- newNode
```
## Add Visualization 
<img src="https://i.imgur.com/AEkoOUG.png"/>
<img src="https://i.imgur.com/iQIA5qP.png"/>
<img src ="https://i.imgur.com/kxmpfsC.png"/>

## Add Big O
- Using above method is O(1) since we are just putting it at start of list

## Can add into middle for Big O(n)
 - [CodeFellowsLinkedList](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

 ## Print
 ``` pseudo
 ALGORITHM Print()
// INPUT <-- None
// OUTPUT <-- string to console

  Current <-- Head

  WHILE Current is not equal to NULL
    OUTPUT <-- "{Current.Value} --> "
    Current <-- Current.Next

  OUTPUT <-- "NULL"
```
## Memory 

<img src = "https://i.imgur.com/V89id7k.png"/>

- The fundamental difference between arrays and linked lists is that arrays are static data structures, while linked lists are dynamic data structures.
-  A static data structure needs all of its resources to be allocated when the structure is created
- dynamic data structure can shrink and grow in memory

## Anatomy 

<img src= "https://i.imgur.com/BvejLtG.png"/>
- A single node has just two parts: 

    1. data
    2. a reference to the next node.

## Array VS Linked List
<img src ="https://i.imgur.com/mWVvrzC.png"/>
<img src = "https://i.imgur.com/DGRQJ5p.png"/>

## Big O graph
<img src = "https://i.imgur.com/LykLjAF.png"/>
<img src = "https://i.imgur.com/izeeV59.png"/>
<img src = "https://i.imgur.com/KbR5Cg6.png"/>