class BST:
    class Node:
        def __init__(self, data):
            self.data = data
            self.left = None
            self.right = None

    def __init__(self):
        self.root = None

    def insert(self, data):
        if self.root is None:
            self.root = BST.Node(data)
        else:
            self._insert(data, self.root)  # Start at the root
    def _insert(self, data, node):
        if data < node.data:
            if node.left is None:
                node.left = BST.Node(data)
            else:
                self._insert(data, node.left)
        elif data > node.data:
            if node.right is None:
                node.right = BST.Node(data)
            else:
                self._insert(data, node.right)
        else:
            print ('Invalid data entered')
    def __contains__(self, data):
        return self._contains(data, self.root)
    def _contains(self, data, node):

        if node is None:
            return False
        elif data == node.data:
            return True
        if data < node.data:
                return self._contains(data, node.left)
        elif data > node.data:
                return self._contains(data, node.right)
    def __iter__(self):
        yield from self._traverse_forward(self.root)
        
    def _traverse_forward(self, node):
        if node is not None:
            yield from self._traverse_forward(node.left)
            yield node.data
            yield from self._traverse_forward(node.right)




            
tree = BST()
tree.insert(6)
tree.insert(13)
tree.insert(2)
tree.insert(4)
tree.insert(10)
tree.insert(5)
tree.insert(7)


length_list = []

def recursive_traverse(node, length_list, length):
    length += 1
    if node == None:
        if len(length_list) == 0:
            length_list.append(length)
        elif length_list[0] < length:
            del length_list[0]
            length_list.append(length)
        else:
            pass
        
        
    elif node != None:
        recursive_traverse(node.right, length_list, length)
        recursive_traverse(node.left, length_list, length)

length = 0
length_list = []

recursive_traverse(tree.root, length_list, length)

print ((length_list[0]-1))

