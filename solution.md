# Solution



## Stack you try problem:

```python
def reverse(list):
    
    # Initialize an empty list
    reverse_list= []

    while len(list):
        # adding numbers to the empty reverse_list in backwards order
        # pop starts at the back of the list(LIFO)
        reverse_list.append(list.pop()) 

    return reverse_list
        

list = [10, 11, 12, 13]
print(reverse(list))

list = ['f', 'l', 'o', 'w']
print(reverse(list))
```



## Linked List you try problem:

```python

def get_value(self, index):

    # Create variables to keep track of the current index and node
    curr_index = 0
    curr_node = self.head

    # Iterate through the list 
    while curr_node != None:

        # Check the curret index 
        if curr_index == index:
            return curr_node.data # Return the data of the node
        else:
            # Move to next node and increment the index
            curr_node = curr_node.next
            curr_index += 1
    
    
    return 'item at index not found' # If the index value given is out of range 
```

## BST you try problem:

```python
 def closest_value(self, target, closest_node):
        current_node = self.root
        return self.find_closest_value(current_node, target, closest_node)

    def find_closest_value(self, current_node, target, closest_node):

        if current_node == None:
            return closest_node
        if abs(target - closest_node) > abs(target - current_node.data):
            closest_node = current_node.data
        if target < current_node.data:
            return self.find_closest_value(current_node.left, target, closest_node)
        elif target > current_node.data:
            return self.find_closest_value(current_node.right, target, closest_node)
        else:
            return closest_node
```

[Back to home page](welcome.md)
