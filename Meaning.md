| **Complexity** | **Meaning** | **Example** | **Worst Case Scenario** |
|----------------|-------------|-------------|-------------------------|
| **O(1)**     | Constant time: The operation takes the same time regardless of the input size. | Accessing an element in an array by its index. | Direct access with no need for any search. |
| **O(n)**     | Linear time: We may need to examine every element in the structure. | Searching for an element in an unsorted array. | The target is at the end or not present, requiring a full scan of all elements. |
| **O(n²)**    | Quadratic time: For each element, every other element is processed. | Bubble Sort with nested loops. | In the worst case (e.g., a list in reverse order), every element is compared with every other element, leading to a large number of operations. |
| **O(log n)** | Logarithmic time: The search space is divided in half at each step. | Binary Search in a sorted array. | Even if the target is found in the last step, only about `log(n)` comparisons are required. |
| **O(n log n)** | Log-linear time: The data is divided into parts (log n steps), but each part requires scanning a portion of the data (n). | Merge Sort or average-case Quick Sort. | All parts of the data are processed across the logarithmic divisions, combining both linear and logarithmic factors. |
| **O(2ⁿ)**    | Exponential time: The number of operations doubles with each additional input element. | Recursive Fibonacci (naive recursion). | The number of steps grows exponentially, making the algorithm impractical for even moderately large inputs. |
