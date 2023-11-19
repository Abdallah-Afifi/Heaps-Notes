# Heaps-Notes


1. **Definition:**
   - A binary heap is a complete binary tree where each node has a key, and the key of each node is either greater than or equal to (max heap) or less than or equal to (min heap) the keys of its children.

2. **Types of Heaps:**
   - Max Heap: Every parent node has a key greater than or equal to the keys of its children.
   - Min Heap: Every parent node has a key less than or equal to the keys of its children.

3. **Operations:**
   - Heapify: The process of converting a binary tree into a heap.
   - Insertion: Adding a new element to the heap while maintaining the heap property.
   - Deletion: Removing the root element from the heap and maintaining the heap property.

4. **Array Representation:**
   - Binary heaps can be efficiently represented using an array, where the parent-child relationship is determined by indices.

5. **Heapify Up and Down:**
   - Heapify Up: Used after inserting an element to maintain the heap property by comparing the element with its parent and swapping if necessary.
   - Heapify Down: Used after deleting the root element to maintain the heap property by comparing the element with its children and swapping if necessary.

6. **Heap Sort:**
   - Heap sort is a comparison-based sorting algorithm that uses a binary heap data structure to build a max heap or min heap and then performs the sorting.

7. **Priority Queues:**
   - Binary heaps are often used to implement priority queues due to their efficient insertion and removal of the highest (max heap) or lowest (min heap) priority element.

8. **Time Complexity:**
   - Building a heap: O(n)
   - Insertion and Deletion: O(log n)

9. **Applications:**
   - Priority scheduling algorithms, Dijkstra's algorithm, Huffman coding, etc., leverage binary heaps for efficient implementation.

10. **Common Mistakes:**
    - Ensure understanding the difference between max and min heaps.
    - Pay attention to index calculations when implementing heap operations.

Certainly! Let's delve into the details of insertion, building, deletion, and removal, along with illustrations on how to calculate the number of comparisons for each operation.

### Insertion:

- **Operation:**
  - Inserting a new element into the heap while maintaining the heap property.

- **Procedure:**
  1. Add the new element at the end of the heap (as the last leaf).
  2. Compare the new element with its parent.
  3. If the heap property is violated (for max heap, child > parent; for min heap, child < parent), swap the elements.
  4. Repeat steps 2-3 until the heap property is restored.

- **Number of Comparisons:**
  - In the worst case, the number of comparisons is the height of the heap, which is O(log n) for a heap with n elements.

### Building (Heapify):

- **Operation:**
  - Converting a binary tree into a heap.

- **Procedure:**
  - Start from the last non-leaf node and heapify each node in reverse level order.
  - Heapify involves comparing the node with its children and swapping if necessary.

- **Number of Comparisons:**
  - The number of comparisons is proportional to the number of nodes in the tree, which is O(n).

### Deletion:

- **Operation:**
  - Removing the root element from the heap while maintaining the heap property.

- **Procedure:**
  1. Replace the root with the last element in the heap.
  2. Compare the new root with its children.
  3. If the heap property is violated, swap with the larger (max heap) or smaller (min heap) child.
  4. Repeat steps 2-3 until the heap property is restored.

- **Number of Comparisons:**
  - Similar to insertion, in the worst case, the number of comparisons is O(log n) where n is the number of elements in the heap.

### Removal (Extracting):

- **Operation:**
  - Extracting the root element from the heap.

- **Procedure:**
  1. Save the root element (the one to be removed).
  2. Replace the root with the last element in the heap.
  3. Compare the new root with its children and swap if necessary.
  4. Repeat steps 3 until the heap property is restored.
  5. Return the saved root element.

- **Number of Comparisons:**
  - Similar to insertion and deletion, in the worst case, the number of comparisons is O(log n) where n is the number of elements in the heap.

Certainly! Here are more notes on the structure of heaps:

### 1. **Complete Binary Tree:**
   - A binary heap is a complete binary tree, meaning all levels of the tree are fully filled, except possibly the last level, which is filled from left to right.

### 2. **Array Representation:**
   - Binary heaps can be efficiently represented using an array.
   - For a node at index i:
      - Its left child is at index 2i + 1.
      - Its right child is at index 2i + 2.
      - Its parent is at index floor((i-1)/2).

### 3. **Height of a Heap:**
   - The height of a heap with n elements is O(log n).
   - The height is the maximum distance from the root to a leaf.

### 4. **Levels and Nodes:**
   - Level i of the heap contains 2^i nodes.
   - The total number of nodes in a heap of height h is 2^(h+1) - 1.

### 5. **Leaf Nodes:**
   - In a heap, all leaf nodes are at the last level or the level just above the last level.
   - Leaf nodes are always filled from left to right.

### 6. **Parent-Child Relationship:**
   - In a max heap, every parent node has a key greater than or equal to the keys of its children.
   - In a min heap, every parent node has a key less than or equal to the keys of its children.

### 7. **Heap Operations Complexity:**
   - Building a heap from an array: O(n)
   - Insertion: O(log n)
   - Deletion (Extracting): O(log n)
   - Heapify (percolate up or down): O(log n)

### 8. **Special Properties:**
   - The smallest (max heap) or largest (min heap) element is always at the root.
   - Successive levels contain elements in non-decreasing (max heap) or non-increasing (min heap) order.

### 9. **Applications:**
   - Priority queues: Binary heaps are commonly used to implement priority queues due to their efficient insertion and removal of the highest or lowest priority element.
   - Heap sort: A sorting algorithm that uses a binary heap to perform the sort.

### 10. **Dynamic Operations:**
   - Heaps are well-suited for dynamic operations like insertions and deletions, as the structure remains balanced.


