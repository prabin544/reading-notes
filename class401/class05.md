## Linked Lists

Linked lists are an ordered collection of objects. Each element of a linked list is called a node, and every node has two different fields:

- Data contains the value to be stored in the node.
- Next contains a reference to the next node on the list.

A linked list is a sequence of data elements, which are connected together via links. Each data element contains a connection to another data element in form of a pointer. Python does not have linked lists in its standard library. We implement the concept of linked lists using the concept of nodes as discussed in the previous chapter. We have already seen how we create a node class and how to traverse the elements of a node. In this chapter we are going to study the types of linked lists known as singly linked lists. In this type of data structure there is only one link between any two data elements. We create such a list and create additional methods to insert, update and remove elements from the list.

1. Start with a single node
Let’s start with a single node since linking several nodes gives us a complete list. For this, we make a Node class that holds some data and a single pointer next, that will be used to point to the next Node type object in the Linked List.  
```
# A single node of a singly linked list
class Node:
  # constructor
  def __init__(self, data, next=None): 
    self.data = data
    self.next = next

# Creating a single node
first = Node(3)
print(first.data)
```
2. Join nodes to get a linked list
The next step is to join multiple single nodes containing data using the next pointers, and have a single head pointer pointing to a complete instance of a Linked List.

Using the head pointer, we will be able to traverse the whole list, even perform all kinds of list manipulations while we are at it.

For this, we create a LinkedList class with a single head pointer:  
```
# A single node of a singly linked list
class Node:
  # constructor
  def __init__(self, data = None, next=None): 
    self.data = data
    self.next = next

# A Linked List class with a single head node
class LinkedList:
  def __init__(self):  
    self.head = None

# Linked List with a single node
LL = LinkedList()
LL.head = Node(3)
print(LL.head.data)
```
3. Add required methods to the LinkedList class
Last but not least, we can add various linked list manipulation methods in our implementation.

Let’s have a look at the insertion and print methods for our LinkedList implementation below:  
```
# A single node of a singly linked list
class Node:
  # constructor
  def __init__(self, data = None, next=None): 
    self.data = data
    self.next = next

# A Linked List class with a single head node
class LinkedList:
  def __init__(self):  
    self.head = None
  
  # insertion method for the linked list
  def insert(self, data):
    newNode = Node(data)
    if(self.head):
      current = self.head
      while(current.next):
        current = current.next
      current.next = newNode
    else:
      self.head = newNode
  
  # print method for the linked list
  def printLL(self):
    current = self.head
    while(current):
      print(current.data)
      current = current.next

# Singly Linked List with insertion and print methods
LL = LinkedList()
LL.insert(3)
LL.insert(4)
LL.insert(5)
LL.printLL()
```  
[Source](https://www.educative.io/edpresso/how-to-create-a-linked-list-in-python)

