## Minimum Spanning Tree
A minimum spanning tree (MST) or minimum weight spanning tree is a subset of the edges of a connected, edge-weighted undirected graph that connects all the vertices together, without any cycles and with the minimum possible total edge weight

![](https://github.com/jongwoojeff/DiscreteMathematics/blob/master/images/minimum-spanning-tree.png)

## Prim's Algorithm
A greedy algorithm that finds a minimum spanning tree for a weighted undirected graph

**Algorithm**
1) Create a set mstSet that keeps track of vertices already included in MST.
2) Assign a key value to all vertices in the input graph. Initialize all key values as INFINITE. Assign key value as 0 for the first vertex so that it is picked first.
3) While mstSet doesn’t include all vertices

   ….a) Pick a vertex u which is not there in mstSet and has minimum key value.

   ….b) Include u to mstSet.

   ….c) Update key value of all adjacent vertices of u. To update the key values, iterate through all adjacent 
   vertices. For every adjacent vertex v, if weight of edge u-v is less than the previous key value of v, update 
   the key value as weight of u-v

## Kruskal's Algorithm
A minimum-spanning-tree algorithm which finds an edge of the least possible weight that connects any two trees in the forest

**Algorithm**

1. Sort all the edges in non-decreasing order of their weight.
2. Pick the smallest edge. Check if it forms a cycle with the spanning tree formed so far. If cycle is not formed, include this edge. Else, discard it.
3. Repeat step#2 until there are (V-1) edges in the spanning tree.

## Huffman Coding
A minimal variable-length character coding based on the frequency of each character

**Algorithm**

1. Create a leaf node for each unique character and build a min heap of all leaf nodes (Min Heap is used as a priority queue. The value of frequency field is used to compare two nodes in min heap. Initially, the least frequent character is at root)

2. Extract two nodes with the minimum frequency from the min heap.

3. Create a new internal node with a frequency equal to the sum of the two nodes frequencies. Make the first extracted node as its left child and the other extracted node as its right child. Add this node to the min heap.

4. Repeat steps#2 and #3 until the heap contains only one node. The remaining node is the root node and the tree is complete.

