## Shortest Path Finder

This C program reads an adjacency matrix representing a graph from a file, shows the adjacency matrix, and finds the shortest path between two vertices using Dijkstra's algorithm with a min-heap.

- int main()
The main function manages the user interface loop. It repeatedly displays a menu and performs actions based on the user's choice until the user decides to exit.

- Heap Functions
initializeMinHeap

void initializeMinHeap(struct MinHeap *minHeap, int capacity)
Initializes a min-heap with a given capacity. Allocates memory for the heap's internal array and sets its initial size to zero.

swapMinHeapNodes
void swapMinHeapNodes(struct Node *x, struct Node *y)
Swaps two nodes in the min-heap.

parentOfHeapNode
int parentOfHeapNode(int i)
Returns the index of the parent node in the heap.

leftChildOfHeapNode

int leftChildOfHeapNode(int i)
Returns the index of the left child node in the heap.

rightChildOfHeapNode

int rightChildOfHeapNode(int i)
Returns the index of the right child node in the heap.

getMinElementFromMinHeap

struct Node getMinElementFromMinHeap(struct MinHeap *minHeap)
Returns the minimum element from the min-heap (the root of the heap).

insertElementToMinHeap

void insertElementToMinHeap(struct MinHeap *minHeap, struct Node element)
Inserts a new element into the min-heap and adjusts the heap to maintain the heap property.

heapify

void heapify(struct MinHeap *minHeap, int i)
Restores the heap property by heapifying the subtree rooted at index i.

extractMinElementFromMinHeap

void extractMinElementFromMinHeap(struct MinHeap *minHeap)
Removes the minimum element from the min-heap and adjusts the heap to maintain the heap property.

- File Reading
readInputFile

void readInputFile()
Reads the adjacency matrix from a file. The file contains lines of the form A-B 1, where A and B are vertices and 1 is the weight of the edge between them. The function updates the global adjacency matrix and the existence array.

- Adjacency Matrix Display
showAdjacencyMatrix

void showAdjacencyMatrix()
Displays the adjacency matrix. If there is no path between two vertices, it shows -.

- Menu Handling
showMenuAndGetChoice

int showMenuAndGetChoice()
Displays a menu and gets a valid choice from the user. Repeats until a valid choice is entered.

- Shortest Path Calculation
printPath

void printPath(int j)
Recursively prints the path from the source vertex to vertex j.

shortestPath

void shortestPath()
Finds the shortest path between two vertices using Dijkstra's algorithm. It initializes distances, inserts the source vertex into the min-heap, and updates distances using the min-heap. It prints the shortest path and its length.
