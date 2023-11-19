# Binary Search Tree (BST) Test
This repository features code designed to evaluate the concurrent behavior of a Binary Search Tree (BST) using multithreading. It enables assessment of the BST's performance with multiple threads concurrently executing operations such as insertion, deletion, and search within the tree structure.

## Overview
The code consists of the following components:
1. ConBST_Test.java: The main class that orchestrates the testing of the BST with multithreading.
2. ThreadID.java: A utility class for obtaining thread-specific IDs.
3. Counter.java: A simple counter utility class used to count thread operations.

## Running the Test
You can run the test by compiling and executing `ConBST_Test.java`. The program takes command-line arguments to specify the number of threads, the prefill size of the tree, and the workload. The workload is defined as a string in the format "C-I-D," where:
- "C" represents the percentage of contains operations(Traversing).
- "I" represents the percentage of insert operations.
- "D" represents the percentage of delete operations.

Example command to run the program:
```shell
java ConBST_Test <num_threads> <prefill_size> <workload>
```
Replace `<num_threads>`, `<prefill_size>`, and `<workload>` with appropriate values.

## Testing Strategy
The code initializes a Binary Search Tree (BST) by creating a tree with a specified number of nodes. The tree is prefilled with random values. Subsequently, the program spawns multiple threads to execute operations based on defined workload percentages. The primary purpose is to measure the throughput of the operations and report the results.

## Output
The program reports the following metrics:
- `num_threads`: The number of threads used for testing.
- `totalOps`: The total number of operations performed.
- `throughput`: The throughput in operations per second (ops/s).

## Example Output
BST_Test:num_threads:<num_threads>:totalOps:<totalOps>:throughput:<throughput> ops/s

## Conclusion
This code facilitates concurrent testing of a binary search tree (BST) to evaluate its behavior with various workloads and analyze its performance in multi-threaded scenarios. Users can customize the number of threads, prefill size, and workload to assess the BST's suitability for specific use cases.

##  Graphs plotted against throughput by varying number of threads with workloads for different locks.

TAS Lock:
![image](https://github.com/Anandn3601/HPC_Assignment-3/assets/91625967/9bd913f7-acbf-438a-83f7-011b0b3ef4cb)

TTAS Lock:
![image](https://github.com/Anandn3601/HPC_Assignment-3/assets/91625967/0815823a-e987-4d34-bb5d-5143dce79839)

TTAS WITH BACKOFF Lock:
![image](https://github.com/Anandn3601/HPC_Assignment-3/assets/91625967/8f247ed2-c012-45a2-b67f-d98c69b5aeb3)

A Lock:
![image](https://github.com/Anandn3601/HPC_Assignment-3/assets/91625967/c41c85c0-753d-451f-bd05-e43c5e7a1c80)

CLH Lock:
![image](https://github.com/Anandn3601/HPC_Assignment-3/assets/91625967/43908f9b-9cd5-4a7b-b1e4-28f73ac6e7c3)

MCS Lock:
![image](https://github.com/Anandn3601/HPC_Assignment-3/assets/91625967/81dbfebb-c09c-4fc4-a663-0a582e34f658)



