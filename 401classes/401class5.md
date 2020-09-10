## Linked Lists
A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

*There are two types of Linked List - Singly and Doubly. We will be implementing a Singly Linked List in this implementation.*

- Singly - Singly refers to the number of references the node has. 
A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

- Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

- Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
- Next - Each node contains a property called Next. This property contains the reference to the next node.
- Head - The Head is a reference type of type Node to the first node in a linked list.
- Current - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.
![Image](https://miro.medium.com/max/1230/1*5wRMqVjLatOGX88VrZgacA.jpeg)

*When traversing a linked list, you are not able to use a foreach or for loop.*
*The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.*

#### Big O
Big O Notation is a way to evaluate the performance of an algorithm based on efficiency - specifically in terms of time and memory
big O notation is used to classify algorithms according to how their run time or space requirements grow as the input size grows.


Linked Lists are similar to arrays 
The biggest differentiator between arrays and linked lists is the way that they use memory in our machines.where arrays require memory in a contiguous block, linked lists do not need to be contiguous because they contain references to the next (and sometimes prior) node in the list. 
The fundamental difference between arrays and linked lists is that arrays are static data structures, while linked lists are dynamic data structures. A static data structure needs all of its resources to be allocated when the structure is created; this means that even if the structure was to grow or shrink in size and elements were to be added or removed, it still always needs a given size and amount of memory. If more elements needed to be added to a static data structure and it didn’t have enough memory, you’d need to copy the data of that array, for example, and recreate it with more memory, so that you could add elements to it.