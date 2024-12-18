1. Problem Definition
Implement a program that compares total cost of splay and mod-splay trees. The total cost is sum of total number of comparisons and total number of rotations.
We have mod-splay algorithm in this project. The algorithm is about frequency of occurrence. Inserted element protect its position, whenever its frequency becomes higher than root that time it must be the root by applying zig-zig or zig-zag rotations.

2. Implementation Details
I started to construct the splay node algorithm. There is a struct to implement splay attributes. This struct define as node with typedef for more convenience.
•	createKey(): Function that creates new node for inserting key into tree.
•	leftRotation(): Implements left rotation logic.
•	rightRotation(): Implements right rotation logic.
•	splay(): Implements the splaying operation, which is a special operation for the splay tree. It uses the leftRotation() and rightRotation() functions. 
•	searchKeySplay(): Function that searches the key if this key already exists in splay tree. The key becomes root after the function is executed.
•	insertKeySplay(): Places the keys according to these basis: 
    1.	If key is greater than its parent, the key must be the right child.
    2.	If key is less than its parent, the key must be the left child.
    3.	The splaying operation is implemented for each key inserted. 
    4.	If the key exists, then just search it.
•	insertKeyModSplay(): If frequency of the key exceeds the root, the key becomes the root. Otherwise, it is inserted without splaying.
•	preorderSplay(): Function to write the splay tree as a preorder.
•	preorderModSplay(): Function to write the mod-splay tree as a preorder. The frequency is printed near the each key.
•	main(): The input file is opened, line is read, the elements are tokenized by commas, and the elements are converted from string to integer. The first pre-order traversal and the total cost of the splay tree are printed, after the mod-splay tree is printed.
