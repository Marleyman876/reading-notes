# Linked List

A linked list is just a data structure that contains [nodes](https://www.tutorialspoint.com/python/python_nodes.htm). Linked lists are not stored in a contiguos location instead they are lionked to pointers.

THe linked list has no strict linear ordering in memroy the ordering of the element are controlled by the data structure that contain each one of the data element.

A linkied list uses a node to wrap each data element. Each node has the knowledge of how to get to the next node.

```py

Simple linked list creation. 
# Node class
class Node:
  
    # Function to initialize the node object
    def __init__(self, data):
        self.data = data  # Assign data
        self.next = None  # Initialize
                          # next as null
  
# Linked List class
class LinkedList:
    
    # Function to initialize the Linked
    # List object
    def __init__(self):
        self.head = None
```

## The Linked List below is created with 3 nodes

```py
# A simple Python program to introduce a linked list
 
# Node class
class Node:
 
    # Function to initialise the node object
    def __init__(self, data):
        self.data = data  # Assign data
        self.next = None  # Initialize next as null
 
 
# Linked List class contains a Node object
class LinkedList:
 
    # Function to initialize head
    def __init__(self):
        self.head = None
 
 
# Code execution starts here
if __name__=='__main__':
 
    # Start with the empty list
    llist = LinkedList()
 
    llist.head = Node(1)
    second = Node(2)
    third = Node(3)
 
    '''
    Three nodes have been created.
    We have references to these three blocks as head,
    second and third
 
    llist.head        second              third
         |                |                  |
         |                |                  |
    +----+------+     +----+------+     +----+------+
    | 1  | None |     | 2  | None |     |  3 | None |
    +----+------+     +----+------+     +----+------+
    '''
 
    llist.head.next = second; # Link first node with second
 
    '''
    Now next of first Node refers to second.  So they
    both are linked.
 
    llist.head        second              third
         |                |                  |
         |                |                  |
    +----+------+     +----+------+     +----+------+
    | 1  |  o-------->| 2  | null |     |  3 | null |
    +----+------+     +----+------+     +----+------+
    '''
 
    second.next = third; # Link second node with the third node
 
    '''
    Now next of second Node refers to third.  So all three
    nodes are linked.
 
    llist.head        second              third
         |                |                  |
         |                |                  |
    +----+------+     +----+------+     +----+------+
    | 1  |  o-------->| 2  |  o-------->|  3 | null |
    +----+------+     +----+------+     +----+------+
    '''
```

## Linked list Traversal

```py
# A simple Python program for traversal of a linked list
 
# Node class
class Node:
 
    # Function to initialise the node object
    def __init__(self, data):
        self.data = data  # Assign data
        self.next = None  # Initialize next as null
 
 
# Linked List class contains a Node object
class LinkedList:
 
    # Function to initialize head
    def __init__(self):
        self.head = None
 
    # This function prints contents of linked list
    # starting from head
    def printList(self):
        temp = self.head
        while (temp):
            print (temp.data)
            temp = temp.next
 
 
# Code execution starts here
if __name__=='__main__':
 
    # Start with the empty list
    llist = LinkedList()
 
    llist.head = Node(1)
    second = Node(2)
    third = Node(3)
 
    llist.head.next = second; # Link first node with second
    second.next = third; # Link second node with the third node
 
    llist.printList()

```

## References

[Linked List Set 1](https://www.geeksforgeeks.org/linked-list-set-1-introduction/)

[Linked List Tutorial](https://www.youtube.com/watch?v=JlMyYuY1aXU)

[Nodes](https://www.tutorialspoint.com/python/python_nodes.htm)