---
title: "Binary Search Tree Visualizer"
description: "An interactive visualization tool for binary search trees created for CS240: Data Structures and Algorithms"
category: class
github_link: https://github.com/Sania3fat/bst-visualizer
course_code: "CS240"
semester: "Fall 2023"
technologies:
  - JavaScript
  - D3.js
  - HTML Canvas
  - CSS
image: /assets/images/bst-project.jpg
---

# Binary Search Tree Visualizer
Course Project for CS240: Data Structures and Algorithms

## Course Context
This project was developed as part of the Data Structures and Algorithms course, focusing on tree data structures and their implementations. The assignment challenged students to create an interactive tool that would help visualize BST operations.

## Project Requirements
- Implement a fully functional Binary Search Tree
- Visualize tree operations (insert, delete, search)
- Demonstrate tree traversal algorithms
- Create an interactive user interface
- Include animation for operations

## Implementation

### Core Features
1. **Interactive Tree Building**
   - Add nodes through user input
   - Auto-balance option for AVL implementation
   - Real-time visualization updates

2. **Operation Visualization**
   - Color-coded nodes for search path
   - Step-by-step animation for insertions
   - Highlight path for element deletion

3. **Traversal Demonstrations**
   - In-order traversal
   - Pre-order traversal
   - Post-order traversal
   - Level-order traversal

### Technical Details
```javascript
class TreeNode {
    constructor(value) {
        this.value = value;
        this.left = null;
        this.right = null;
        this.height = 1;
    }
}

class BST {
    constructor() {
        this.root = null;
    }
    
    // Example method
    insert(value) {
        this.root = this._insertRecursive(this.root, value);
    }
    
    _insertRecursive(node, value) {
        if (!node) return new TreeNode(value);
        
        if (value < node.value)
            node.left = this._insertRecursive(node.left, value);
        else if (value > node.value)
            node.right = this._insertRecursive(node.right, value);
            
        return node;
    }
}
```

## Learning Outcomes
Through this project, I gained:
- Deep understanding of BST operations and complexity
- Experience with recursive algorithms
- Skills in interactive visualization development
- Practice with JavaScript and D3.js
- Understanding of algorithm animation techniques

## Challenges Faced
1. **Balancing Visualization and Performance**
   - Challenge: Maintaining smooth animations while handling large trees
   - Solution: Implemented frame-rate control and operation queuing

2. **Tree Layout Algorithm**
   - Challenge: Preventing node overlap in visualization
   - Solution: Developed a level-based spacing algorithm

## Results
The project successfully demonstrates:
- Clear visualization of BST operations
- Interactive learning tool for tree concepts
- Efficient implementation of core operations
- Smooth animations for all tree modifications

### Performance Metrics
| Operation | Time Complexity | Space Complexity |
|-----------|----------------|------------------|
| Insert    | O(log n)       | O(1)            |
| Delete    | O(log n)       | O(1)            |
| Search    | O(log n)       | O(1)            |

## Future Improvements
1. Add support for Red-Black trees
2. Implement tree balancing visualizations
3. Add comparison mode between different tree types
4. Create save/load functionality for tree states

## References
1. Cormen, T. H., et al. (2009). Introduction to Algorithms, 3rd Edition
2. Course materials from CS240
3. D3.js documentation for tree visualization

## Project Grade
**Final Grade: A**
- Implementation: 35/35
- Documentation: 25/25
- Visualization: 30/30
- Code Quality: 10/10

## Acknowledgments
Special thanks to:
- Professor Smith for project guidance
- Teaching Assistant Jane Doe for implementation feedback
- The D3.js community for visualization resources
