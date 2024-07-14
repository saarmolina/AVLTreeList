# AVLTreeList: 
This project is a Python implementation of an AVL Tree List, showcasing advanced skills in data structure manipulation and algorithm design. It highlights my understanding of self-balancing binary search trees, particularly AVL trees, and their use in efficiently maintaining sorted data structures. The implementation covers key computer science concepts, including tree rotations, balance factor maintenance, and operations such as insertions, deletions, and lookups, all achieving optimal time complexity.

## Features

- **AVLNode Class**: Represents individual nodes in the AVL tree with methods for getting and setting node properties.
- **AVLTree Class**: Implements the AVL tree structure with methods for insertion, deletion, searching, and tree balancing.
- **Self-Balancing**: Automatically maintains balance after insertions and deletions to ensure O(log n) time complexity for basic operations.
- **Tree Operations**: Includes methods for joining trees, splitting trees, and converting the tree to a sorted array.

## Key Methods

### AVLNode

- `get_left()`, `get_right()`, `get_parent()`: Retrieve child and parent nodes.
- `get_key()`, `get_value()`, `get_height()`, `get_bf()`: Get node properties.
- `set_left()`, `set_right()`, `set_parent()`: Set child and parent nodes.
- `set_key()`, `set_value()`, `set_height()`: Set node properties.
- `is_real_node()`: Check if the node is not virtual.

### AVLTree

- `insert(key, val)`: Insert a new key-value pair into the tree.
- `delete(node)`: Remove a node from the tree.
- `search(key)`: Find a node with the given key.
- `split(node)`: Split the tree at a given node.
- `join(tree2, key, val)`: Join two AVL trees with a separating key.
- `avl_to_array()`: Convert the tree to a sorted array of key-value pairs.
- `size()`: Get the number of items in the tree.

## Time Complexity

- Insertion: O(log n)
- Deletion: O(log n)
- Search: O(log n)
- Join: O(log n)
- Split: O(log n)

Where n is the number of nodes in the tree.

## Usage

To use this AVL tree implementation, import the `AVLTree` class and create an instance:

```python
from avl_tree import AVLTree

# Create a new AVL tree
tree = AVLTree()

# Insert some key-value pairs
tree.insert(5, "five")
tree.insert(3, "three")
tree.insert(7, "seven")

# Search for a key
node = tree.search(3)
if node:
    print(node.get_value())  # Output: "three"

# Delete a node
node_to_delete = tree.search(5)
if node_to_delete:
    tree.delete(node_to_delete)

# Convert tree to sorted array
sorted_array = tree.avl_to_array()
print(sorted_array)  # Output: [(3, "three"), (7, "seven")]
