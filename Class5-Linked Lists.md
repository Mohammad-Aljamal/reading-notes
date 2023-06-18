# Linked Lists

## [Big O: Analysis of Algorithm Efficiency](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html)


Big O notation is a tool used to measure the efficiency of algorithms in terms of their running time and memory space usage. It focuses on the worst-case scenario to analyze the algorithm's performance. Four key areas are considered in the analysis: input size, units of measurement for running time, units of measurement for memory space, and sources of memory usage. The input size refers to the size of the parameters read by the algorithm. Different units of measurement, such as milliseconds, number of operations executed, or number of basic operations, are used to quantify running time. Memory space is evaluated based on the space required for the code, input data, output data, and working space. It's important to analyze time complexity and space complexity separately, and note that with modern computing capabilities, space complexity is often less of a concern.

#### Orders of Growth
1. Constant Complexity O(1).
2. Logarithmic Complexity O(log n).
3.  Linear Complexity O(n).
4. Linearithmic Complexity O(n log n).
5. Quadratic Complexity O(n^2).
6. Cubic Complexity O(n^3).
7. Exponential Complexity O(2^n).
8. Factorial Complexity O(n!).



## [Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

A linked list is a data structure composed of nodes, where each node contains data and a reference (or pointer) to the next node. The first node is called the head, and the last node points to null. To traverse a linked list, we start from the head and follow the next pointers until we reach null. Insertion and deletion operations in a linked list can be efficient by adjusting the pointers to rearrange the links between nodes. However, direct access to an element requires traversing the list from the beginning, resulting in linear time complexity. Linked lists are useful when dynamic size changes or efficient insertion and deletion operations are required, but random access is not necessary. They are commonly used to implement stacks, queues, and other data structures.


There are several types of linked lists commonly used in programming:

1. Singly Linked List: Each node in this type of linked list contains data and a pointer to the next node in the sequence.

2. Doubly Linked List: In addition to the data and the pointer to the next node, each node in a doubly linked list also has a pointer to the previous node, allowing for traversal in both directions.

3. Circular Linked List: In a circular linked list, the last node points back to the first node, creating a circular structure. This allows for continuous traversal through the list without reaching null.

4. Skip List: A skip list is a type of linked list that uses multiple parallel linked lists with different skip distances. This structure enables efficient searching by skipping nodes in the list.

5. Self-Organizing Linked List: This type of linked list reorganizes itself based on the frequency of element access. The goal is to optimize the search time for frequently accessed elements.

6. Unrolled Linked List: In an unrolled linked list, multiple elements are stored in each node, resulting in improved cache performance and reduced overhead compared to traditional linked lists.
