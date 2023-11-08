# Matrix Multiplication in Java

## Introduction

This repository focuses on matrix multiplication in the Java programming language. Matrix multiplication is a fundamental operation in linear algebra and finds a wide range of applications in fields like physics, computer science, statistics, and more. While matrix multiplication may appear as a straightforward operation, it can be scientifically complex due to numerous strategies and optimizations that can be applied.

## Repository Contents

This repository is divided into two projects:

### Project 1: Matrix Multiplication Implementations in Java

In this project, you'll find various Java implementations of matrix multiplication, each employing a different approach. Some of the included methods are:

- **Atomic Multiplication:** A simple matrix multiplication implementation without parallelization.
- **Block Multiplication:** Divides matrices into blocks and multiplies each block independently to enhance performance.
- **Executor Service:** Utilizes the ExecutorService framework to parallelize matrix multiplication.
- **Row-Wise Multiplication:** Multiplies rows of the first matrix by columns of the second matrix in parallel.
- **Semaphore Usage:** Implements semaphores to synchronize and control access to shared resources in matrix multiplication.
- **Standard Multiplication:** Traditional matrix multiplication in a single thread.
- **Multiplication with Streams:** Utilizes Java Streams to perform matrix multiplication more concisely.
- **Transposed Multiplication:** Performs transposition of the second matrix to enhance multiplication efficiency.

### Project 2: Tiled Matrix Multiplication

In this project, we specifically focus on "Tiled Matrix Multiplication,"  a specialized technique employed to optimize matrix multiplication. It involves breaking down large matrices into smaller submatrices, enabling more efficient and parallel processing.

Instead of directly multiplying two complete matrices, as in traditional matrix multiplication, the segmented approach divides matrices into blocks or "tiles." Each of these smaller blocks is multiplied and summed to obtain the final result. This strategy proves particularly beneficial when working with large matrices or when high computational performance is required.

Matrix segmentation and block-wise multiplication effectively leverage modern hardware architectures and parallelization, potentially resulting in significant improvements in computation speed. This is especially critical in applications that demand intensive matrix processing, such as machine learning and scientific computing.

## Matrix Multiplication Complexity

Matrix multiplication is a fundamental operation in linear algebra and is widely used in various scientific and engineering applications. The complexity of this calculation is based on the number of operations required to perform the multiplication.

In the context of computational complexity notation, the "O" notation (Big O notation) is used to describe the algorithm's complexity. For matrix multiplication, the complexity is typically O(n^3), where "n" represents the size of the square matrices involved. This means that the time required for matrix multiplication increases rapidly as the size of the matrices grows.

The O(n^3) complexity arises from the fact that when multiplying two n x n matrices, n^3 individual operations are necessary. Each element of the resulting matrix is computed by multiplying a row of the first matrix by a column of the second matrix and summing the products. This involves n multiplications and n-1 additions for each element, resulting in n * (n multiplications + n-1 additions) operations per element. Since there are n^2 elements in the resulting matrix, the total complexity is O(n^3).

## Using the Repository

Inside each project, you will find Java source code that implements the various matrix multiplication methods or "Tiled Matrix Multiplication." You can explore and run this code to compare their performance and efficiency in different scenarios.

## Personal information
I am a student currently in my last year of study at the University of Las Palmas de Gran Canaria (ULPGC). My academic focus is on data science and engineering, with a passion for research and development in the field of Deep Learning.

If you want to know more about my experience and work, you can visit my LinkedIn profile https://www.linkedin.com/in/victoria-torres-rodriguez-199a67230/.
