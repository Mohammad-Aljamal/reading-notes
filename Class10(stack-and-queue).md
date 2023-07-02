# Class 10


##  [STACK and QUEUE](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)



### STACK

The primary characteristic of the stack is LIFO (Last-In-First-Out) and FILO (First-In-Last-Out).
The Stack Data-Structure can be represented as a stach of pringles chips.
It contain a multi basic operations:
     Push: to add an element to the top of the stack.
     Pop: to remove an element from the top of the stack.
           note: (in the pop we should check if the Stack is empty to avoid any error)
     isEmpty: to check if the Stack is empty or not.
     peek: to get the value of the top node (last node in the stack).

The Big-O of all this operations is O(1).
The first node.next pointed to Null & last node.next pointed to the previous node.

[](./assets/stack.png)




### QUEUE

The primary characteristic of the Queue is FIFO (First-In-First-Out) and LILO (Last-In-Last-Out).
The queue Data-Structure can be represented as a line of people standing to order.
It contain a multi basic operations:
    enqueue: to add an element to the rear of the Queue (as a last node).
    dequeue: to remove an element from the front of the Queue.
           note: (in the dequeue we should check if the Queue is empty to avoid any error)
    isEmpty: to check if the Queue is empty or not.
    peek: to get the value of the front node (first node in the Queue).

The Big-O of all this operations is O(1).
The first node (front.next) pointed to the second node & last node (rear.next) pointed to the Null.

[](./assets/queue.png)
