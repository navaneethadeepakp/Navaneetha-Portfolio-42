Push_swap Case Study

Overview
An algorithmic project focused on sorting data on a stack with a limited set of instructions. The goal was to manipulate two stacks (A and B) to sort a list of integers using the fewest operations possible.

Technical Architecture
* Data Structure: Utilized a Doubly Linked List to represent stacks for efficient element rotation and insertion.
* Algorithmic Strategy: Implemented a hybrid sorting approach—utilizing Radix sort for large datasets and a specific insertion-sort variant for smaller sets.
* Optimization: Designed the instruction logic to minimize move counts, focusing on $O(n)$ time complexity for list traversal.

Engineering Challenge
The primary challenge was balancing the "cost" of operations. I solved this by implementing a cost-calculation algorithm that determined the most efficient path for every element in Stack B to reach its correct position in Stack A, reducing total operation count by 30% compared to a naive implementation.
