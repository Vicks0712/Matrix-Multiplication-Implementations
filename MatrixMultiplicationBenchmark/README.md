
# Project: Matrix Multiplication Benchmark

## Project Overview

The objective of this project is to explore and compare various methods of matrix multiplication, both parallel and non-parallel. Some of the methods examined include atomic, block-based, executor service, semaphores, row-wise, streams, threads, and transposed matrix multiplication, among others.

## Code Modules and Classes

### Builders
- `DenseMatrixBuilder.java`: This class is responsible for constructing dense matrices, which are regular matrices where most of the elements are non-zero.
- `SparseMatrixCCSBuilder.java`: This builder is used for constructing sparse matrices in Compressed Column Storage (CCS) format.
- `SparseMatrixCOOBuilder.java`: This builder is used for constructing sparse matrices in Coordinate List (COO) format.
- `SparseMatrixCRSBuilder.java`: This builder is used for constructing sparse matrices in Compressed Row Storage (CRS) format.

### Deserializers
- `COOfromMTXtoDenseMatrixObjectDeserializer.java`: This class handles the deserialization of matrices in COO format from MTX files into dense matrices.
- `COOfromMTXtoSparseMatrixCOOObjectDeserializer.java`: This class handles the deserialization of matrices in COO format from MTX files into sparse matrices.

### Matrix Classes
- `DenseMatrix.java`: This class represents a dense matrix, a regular matrix with most elements populated.
- `SparseMatrixCCS.java`: Represents a sparse matrix in Compressed Column Storage format.
- `SparseMatrixCOO.java`: Represents a sparse matrix in Coordinate List format.
- `SparseMatrixCRS.java`: Represents a sparse matrix in Compressed Row Storage format.

### Operations

#### Parallelism

##### Executor Service
- `ESDenseMatrixMultiplication.java`: Provides parallel matrix multiplication using the Executor Service framework for dense matrices.
- `ESSparseMatrixMultiplication.java`: Provides parallel matrix multiplication using the Executor Service framework for sparse matrices.

##### Streams
- `StreamDenseMatrixMultiplication.java`: Enables parallel matrix multiplication using Java streams for dense matrices.
- `StreamSparseMatrixMultiplication.java`: Enables parallel matrix multiplication using Java streams for sparse matrices.
- `StreamsDenseMatrixMultiplication.java`: Offers parallel matrix multiplication using Java streams for dense matrices.

#### Sequential
- `RowMatrixMultiplication.java`: Performs matrix multiplication sequentially using row-wise multiplication.
- `SparseMatrixMultiplication.java`: Handles sequential matrix multiplication for sparse matrices.
- `StandardMatrixMultiplication.java`: Provides sequential matrix multiplication using the standard method.
- `TransposedMatrixMultiplication.java`: Performs sequential matrix multiplication using the transposed method.

#### Synchronization

##### Atomic
- `AtomicDenseMatrix.java`: Represents an atomic dense matrix.
- `AtomicDenseMatrixMultiplication.java`: Offers matrix multiplication with atomic operations for dense matrices.

##### Blocks
- `BlockTask.java`: Represents a task for block-based matrix multiplication.
- `ConcurrencyManager.java`: Manages concurrent block multiplication tasks.
- `SBMatrixMultiplication.java`: Provides matrix multiplication using block-based synchronization.
- `ThreadManager.java`: Manages concurrent threads for block-based synchronization.

##### Semaphores
- `ParallelSemaphoreDenseMatrixMultiplication.java`: Enables parallel matrix multiplication using semaphores for dense matrices.
- `ParallelSemaphoreSparseMatrixMultiplication.java`: Offers parallel matrix multiplication using semaphores for sparse matrices.

##### Threads
- `ParallelMatrixMultiplication.java`: Handles parallel matrix multiplication using threads.
- `ThreadTask.java`: Represents a task to be executed in a separate thread.

## Benchmarking

The project includes benchmarking to assess performance and results, utilizing Java's testing capabilities. The provided code for benchmarking consists of test cases that evaluate the various matrix multiplication methods.

### DenseMatrixMultiplicationTest

This test suite evaluates the multiplication of two random dense matrices using different algorithms, including the standard algorithm, row-wise multiplication, transposed multiplication, streams, Executor Service, threads, synchronized blocks, semaphores, and atomic operations. It covers matrix sizes of 10, 100, and 1000.

### BigSparseMultiplicationTest

This test focuses on the multiplication of two MTX compressed matrices. It reads a specific MTX file (e.g., pdb1HYS.mtx), converts it into a suitable format, and multiplies the matrices using the Sparse Matrix Multiplication method. The result is then compared to the multiplication of dense matrices for verification.

Please ensure you have the required dependencies and configurations in place to run these tests effectively.

### Execution Time Parallel vs Sequential Methods
The benchmark results are presented in the graphical representation below. Each bar represents the average execution time of the respective matrix multiplication operation type across different matrix sizes
<p align="center">
  <img src="https://github.com/Vicks0712/Matrix-Multiplication-Implementations/assets/90756558/2d9cfb53-8b79-41aa-9a0f-a3a1c01d1dec" alt="Benchmark Results" />
</p>
The benchmark clearly illustrates the comparative performance of each matrix multiplication operation type under different scenarios.

## Usage

To utilize this project, follow these steps:

1. Ensure you have the necessary dependencies and configurations in place.
2. Run the specific test cases for the matrix multiplication methods you want to evaluate.

## Contributions

Contributions to this project are highly encouraged and welcomed. If you wish to enhance the code, rectify errors, or introduce new features, please do not hesitate to submit a pull request.
