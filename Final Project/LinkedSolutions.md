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

linked_list = create_linked_list(12345678)


current = linked_list
linked_into_list = []
while current != None:
    linked_into_list.append(current.value)
    current = current.next

middle_number = 0
print(len(linked_into_list) + 1) 
if (len(linked_into_list) % 2 != 0):
    middle_number = linked_into_list[int((len(linked_into_list)) / 2)]
else:
    middle_number = linked_into_list[int((len(linked_into_list) / 2) - 1)]

print(middle_number)
    
