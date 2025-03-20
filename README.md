# Time Complexity Guide

## Sorting Algorithms

### Bubble Sort
- **Best Case:** `O(n)` – Already sorted; only one pass needed.
- **Average Case:** `O(n^2)` – Half swaps required on average.
- **Worst Case:** `O(n^2)` – Reverse order requires full swaps.

### Selection Sort
- **Best Case:** `O(n^2)` – Always scans full list per iteration.
- **Average Case:** `O(n^2)` – No improvement in general cases.
- **Worst Case:** `O(n^2)` – Same as average, always iterates.

### Insertion Sort
- **Best Case:** `O(n)` – Already sorted; inserts in place.
- **Average Case:** `O(n^2)` – Elements shift till correct position.
- **Worst Case:** `O(n^2)` – Reverse order requires full shifts.

### Merge Sort
- **Best Case:** `O(n log n)` – Always splits & merges efficiently.
- **Average Case:** `O(n log n)` – Always divides into halves.
- **Worst Case:** `O(n log n)` – Even worst case follows split-merge.

### Quick Sort
- **Best Case:** `O(n log n)` – Ideal pivot selection every time.
- **Average Case:** `O(n log n)` – On average, good pivots reduce size by half.
- **Worst Case:** `O(n^2)` – Worst pivot (e.g., smallest element) leads to unbalanced splits.

---

## Searching Algorithms

### Linear Search
- **Best Case:** `O(1)` – Found in first position.
- **Average Case:** `O(n)` – Must check half elements on average.
- **Worst Case:** `O(n)` – Must check all elements.

### Binary Search
- **Best Case:** `O(1)` – Found at middle index.
- **Average Case:** `O(log n)` – Always halves search space.
- **Worst Case:** `O(log n)` – Always halves search space even in worst case.

---

## Graph Algorithms

### Breadth-First Search (BFS)
- **Best Case:** `O(1)` – Start node is the goal.
- **Average Case:** `O(V + E)` – Must visit most nodes & edges.
- **Worst Case:** `O(V + E)` – Fully connected graph requires visiting all nodes.

### Depth-First Search (DFS)
- **Best Case:** `O(1)` – Goal found in first path explored.
- **Average Case:** `O(V + E)` – Visits each node and edge once.
- **Worst Case:** `O(V + E)` – Must traverse entire graph if no cycles.

### Dijkstra’s Algorithm
- **Best Case:** `O(V log V + E)` – Optimal path found early in sparse graphs.
- **Average Case:** `O(V log V + E)` – Priority queue efficiently finds shortest path.
- **Worst Case:** `O(V^2)` – Dense graphs slow down priority queue updates.

---

## Tree Operations

### Binary Tree Traversal (Inorder, Preorder, Postorder)
- **Best Case:** `O(n)` – Always visits every node.
- **Average Case:** `O(n)` – Every node visited once.
- **Worst Case:** `O(n)` – Even worst case requires full traversal.

### Binary Search Tree (BST) Search
- **Best Case:** `O(1)` – Root holds the target value.
- **Average Case:** `O(log n)` – Balanced tree ensures logarithmic search.
- **Worst Case:** `O(n)` – Skewed tree behaves like a linked list.

### AVL Tree (Search, Insert, Delete)
- **Best Case:** `O(log n)` – Height always balanced.
- **Average Case:** `O(log n)` – Logarithmic due to rebalancing.
- **Worst Case:** `O(log n)` – Rotations maintain balanced structure.

---

## Heap Operations

### Insert
- **Best Case:** `O(1)` – Insert at end; no swaps.
- **Average Case:** `O(log n)` – Swap up half the time.
- **Worst Case:** `O(log n)` – Full swaps up the heap.

### Delete (Extract Min/Max)
- **Best Case:** `O(1)` – Root removed, no swaps.
- **Average Case:** `O(log n)` – Heapify restores order.
- **Worst Case:** `O(log n)` – Full swaps down heap required.

### Build Heap
- **Best Case:** `O(n)` – Efficient bottom-up construction.
- **Average Case:** `O(n)` – Heapify ensures linear time.
- **Worst Case:** `O(n)` – Always follows heapify process.

---

## Dynamic Programming

### Fibonacci (Recursion)
- **Best Case:** `O(1)` – First two terms already known.
- **Average Case:** `O(2^n)` – Each call splits into two.
- **Worst Case:** `O(2^n)` – Exponential growth due to redundant calls.

### Fibonacci (DP)
- **Best Case:** `O(1)` – Direct lookup.
- **Average Case:** `O(n)` – Memoization avoids redundant work.
- **Worst Case:** `O(n)` – Still needs to compute all terms once.

### Knapsack (0/1)
- **Best Case:** `O(1)` – Small items fit exactly.
- **Average Case:** `O(nW)` – DP table fills row by row.
- **Worst Case:** `O(nW)` – Must compute all subproblems.

---

## String Algorithms

### Naive String Matching
- **Best Case:** `O(n)` – Match found early.
- **Average Case:** `O(nm)` – Must scan part of text for match.
- **Worst Case:** `O(nm)` – Must check all possible shifts.

### KMP Algorithm
- **Best Case:** `O(m)` – Uses precomputed prefix table.
- **Average Case:** `O(n + m)` – Skips unnecessary comparisons.
- **Worst Case:** `O(n + m)` – Always follows prefix function strategy.

### Rabin-Karp
- **Best Case:** `O(m)` – Hash match found immediately.
- **Average Case:** `O(n)` – Rolling hash reduces comparison count.
- **Worst Case:** `O(nm)` – Many hash collisions slow it down.
- 


| **Complexity** | **Meaning** | **Example** | **Worst Case Scenario** |
|----------------|-------------|-------------|-------------------------|
| **O(1)**     | Constant time: The operation takes the same time regardless of the input size. | Accessing an element in an array by its index. | Direct access with no need for any search. |
| **O(n)**     | Linear time: We may need to examine every element in the structure. | Searching for an element in an unsorted array. | The target is at the end or not present, requiring a full scan of all elements. |
| **O(n²)**    | Quadratic time: For each element, every other element is processed. | Bubble Sort with nested loops. | In the worst case (e.g., a list in reverse order), every element is compared with every other element, leading to a large number of operations. |
| **O(log n)** | Logarithmic time: The search space is divided in half at each step. | Binary Search in a sorted array. | Even if the target is found in the last step, only about `log(n)` comparisons are required. |
| **O(n log n)** | Log-linear time: The data is divided into parts (log n steps), but each part requires scanning a portion of the data (n). | Merge Sort or average-case Quick Sort. | All parts of the data are processed across the logarithmic divisions, combining both linear and logarithmic factors. |
| **O(2ⁿ)**    | Exponential time: The number of operations doubles with each additional input element. | Recursive Fibonacci (naive recursion). | The number of steps grows exponentially, making the algorithm impractical for even moderately large inputs. |

