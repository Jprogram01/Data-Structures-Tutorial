# Problem One

Reverse a Linked List

Given a linked list, reverse the order of it in a new list.

class Node:
    def __init__(self, value=0, next=None):
        self.value = value
        self.next = next

def create_linked_list(num):
    head = Node()
    current = head
    string_number = str(num)

    for i in range(len(string_number)):
        current.next = Node(int(string_number[i]))
        current = current.next

    return head.next

linked_list = create_linked_list(30214)

current = linked_list
reversed_list = []
while current != None:
    reversed_list.insert(0, current.value)
    current = current.next

print(reversed_list)


# Problem Two

Find the middle of a linked list

Given a linked list, find the middle of it. If the list is even in its amount give the first of the middle numebrs.

class Node:
    def __init__(self, value=0, next=None):
        self.value = value
        self.next = next

def create_linked_list(num):
    head = Node()
    current = head
    string_number = str(num)

    for i in range(len(string_number)):
        current.next = Node(int(string_number[i]))
        current = current.next

    return head.next

linked_list = create_linked_list(123456789)

