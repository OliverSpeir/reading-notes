# Array Vs Linked List
- Array is static 
- Linked List is dynamic
- References: [Linked List Notes](https://github.com/OliverSpeir/Reading-Notes/blob/main/401/LinkedListNotes.md)
## Static
- This means that when it is created it has a fixed size 
- All the memory is stored together 
- <img src = "https://i.imgur.com/V89id7k.png"/>
- When it needs to be increased a new array is actually made with larger memory allocation and the existing data is added to the new one
    - This can have BigO implications as more processes are done when adding 
        - if data needs to be added too often array might not be best choice

## Dynamic 
- It can grow as needed 
- Memory is not allocated in contiguous block


## Pros and Cons

<img src ="https://i.imgur.com/mWVvrzC.png"/>
<img src = "https://i.imgur.com/DGRQJ5p.png"/>