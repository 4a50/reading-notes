# Notes for Read 05 - Linked Lists

## Linked Lists

[CodeFellows - Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

A Link list is a series of data called **nodes** that chained together either *doubly* or *singly*.

If it is *singly* it only knows the *NEXT* node ahead
If it is *doubly* it know the *PREVIOUS* & the *NEXT* node ahead of it.

The start is called the *Head* and the end is called the *tail*.   Like a dragon.

There is also a *reference* node, that tracks which node is getting looked at.

To iterate through *linked-list* **Foreach** and **for** loops won't work.
Have to use a **while**.  The reason is that you NEED to be able determine if the *NEXT* is a null or not.

So, with a linked list you CAN'T just hop to the center and add something.
If you wanted to add something, iterate to the spot you want to add the data.  Set the new data's **NEXT** to the current node's **NEXT**

THEN you have to change current node's **NEXT** to the NEW node.

### Big O : 
Time: O(n)  <-- n being the number of Node possible
Space O(1), because it won't take any more memory than was alloted to it.

## What is a Linked List Anyway? [Part 1]

[Article](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

This article covers a some important concepts.  
First a Linked list is a dynamic data structure.  An Array is a static data structure, meaning that it needs all the memory for it's 
size in a contiguous block.  If you need to add to it.  You need to copy it to a bigger array and add the data you need.

A the nodes in a linked list has the Value and the reference to the next node of data, so the linked list can exsist in any open 
areas of memory.

There are a few kinds of linked lists.

Circular = The Tail points to the head.
Singly and Doubly, as described above.

## What is a Linked List Anyway? [Part 2]
[Article](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

This article talks a about BigO notation.  
O(1) is what you want. Constant time.  
O(n) will take as long as the number of elements
O(n^2) will take exponentially as long as the number of elements.

You can't search quickly through a linked-list.
It will also take a long time to add something to the end of the list, because you have to travel through the entire list to get there.

They aren't the answer to all you needs, but they are good for adding things to the beginning, and are dynamic.
Arrays are OK too.



[&lt;--&#91;BACK&#93;](/README.md)