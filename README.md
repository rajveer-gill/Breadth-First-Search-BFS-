# Breadth-First Search (BFS) Implementation

## Overview

This repository contains an implementation of the Breadth-First Search (BFS) algorithm using two approaches:

1. **Linked List Representation:**  
   - Constructs an adjacency list from an adjacency matrix.
   - Performs BFS using the adjacency list representation.

2. **Sparse Matrix-Vector Multiplication (SpMV):**  
   - Uses an adjacency matrix to implement BFS via matrix-vector multiplication.

## Features

### Graph Representation
- Constructs adjacency lists from matrices.
- Supports graph traversal using BFS.
- Handles large graphs efficiently.

### Matrix Operations
- Loads adjacency matrices from text files.
- Performs matrix transposition for SpMV-based BFS.

### Input/Output
- Reads adjacency matrix from input files.
- Outputs computed BFS distances to result files.

## File Overview

### Source Files
- **`graph.c` / `graph.h`**  
  - Handles adjacency list operations such as creation, addition, and traversal.
  - Implements BFS using the adjacency list.

- **`matrix.c` / `matrix.h`**  
  - Provides matrix operations like transposition and vector manipulation.
  - Implements BFS using the SpMV method.

- **`load.c` / `load.h`**  
  - Contains functions to load adjacency matrices and save BFS results.

- **`main.c`**  
  - The entry point of the program, orchestrating file loading, BFS execution, and result storage.

### Build System
- **`Makefile`**  
  - Build system to compile the project using `gcc` with the `-std=c11` flag.

## Usage

### Compilation

To compile the program, run:
make

### Execution
To execute the program:
./bfs <matrix_file> <source_vertex>

Example:
./bfs test1.txt 0

## Testing
### Input Files
test1.txt, test2.txt - contain adjacency matrices.

### Output Files
ans_X.txt - expected BFS distance results for source vertex X.

### Verification
Compare your output with the provided answer files using the diff command:
diff distance_0_LL.txt ans_0.txt

## Notes
Do not hard-code file names; they should be passed as command-line arguments.
Ensure your implementation adheres to the provided function headers.
The provided Makefile ensures compatibility with the -std=c11 standard.

## License
This project is for educational purposes.



