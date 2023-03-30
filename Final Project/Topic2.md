# Linked List

A linked list is a data structure made up of nodes. Each node holds a piece of data, and either one or two connections. A single connection will point to the next node, if their is two the other node will point to the previous node.

In Python the node set up can look something like:

class Node:
    def __init__(self, value=0, next=None):
        self.value = val
        self.next = next

What this looks like in picture form is:

![LinkedList](linkedlist.png)

The first node of a linked list is called the head, and the end node is call the tail. 

(Problem Solving Using Linked List)[Final Project/LinkedProblems.md]


Another useful data structure is a hashmap. A hashmap is a data structure which is very similar to a list. A hashmap stores information buy a key, and then the information stored can be accessed by that key.