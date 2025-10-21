## Generalized Linked List (GLL) Menu-Driven Program
This is a simple, menu-driven C program for creating, managing, and displaying a Generalized Linked List (GLL). A GLL is a list that can contain either atomic data (integers, in this case) or other lists (sublists), allowing for complex, nested, recursive data structures.

This program provides a command-line interface to dynamically build a GLL and display its nested structure.

📜 Data Structure
The core of the program is the struct Node. A flag variable is used to differentiate between two types of nodes:

Data Node (flag == 0): Holds an integer value in the data field.

Sublist Node (flag == 1): Holds no data itself, but its sublist pointer points to the head of another linked list.


C :
struct Node {
    int flag; // 0 for data, 1 for sublist
    int data; // Used if flag is 0
    struct Node* sublist; // Used if flag is 1
    struct Node* next; // Pointer to the next node in the current list
};

✨ Features
Add Data: Append integer data nodes to the main list (or any sublist).

Add Sublists: Append new sublist nodes, which you can then populate recursively.

Recursive Building: A sub-menu allows you to build nested lists to any depth.

Recursive Display: A single display function can traverse and print the entire complex structure in a human-readable format (e.g., [ 10, [ 20, 30 ], 40 ]).
