All this sets up a tree called a binary tree. The way it works is it stores numbers. Numbers less than a parent node will go to the "left" and numbers greater than a parent node will go to the "right"

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


# Problem 1

Find the greatest number within the tree.


## Solution

def recursive_traverse(node, length_list):
    if node == None:
        pass
        
        
    elif node != None:
        if len(length_list) == 0:
            length_list.append(node.data)
        else:
            del length_list[0]
            length_list.append(node.data)
        recursive_traverse(node.right, length_list)

length_list = []

recursive_traverse(tree.root, length_list)

print (length_list[0])

# Problem 2

Find the length of the longest branch within a tree