# Tiled Matrix Multiplication

Matrix multiplication is a fundamental operation in linear algebra and is used in a variety of applications, from computer graphics to machine learning. "Tiled Matrix Multiplication" is a technique used in this project to efficiently and distributively calculate matrix multiplication. Here are some key points:

## How does Tiled Matrix Multiplication work?

1. Dividing the matrices into tiles: Instead of multiplying the original matrices directly, they are divided into smaller blocks or "tiles". These tiles are stored in memory and used to perform calculations.
![setup-2d0f22ecd2e9b7c84af56792d14ba18a](https://github.com/Vicks0712/MatrixMultiplicationImplementations/assets/90756558/1b31ec4b-cd02-44c9-a42b-6de0ee2f2fb5)
2. Calculation of tile products: Instead of multiplying the entire matrix A by matrix B at once, the products of the individual tiles are calculated. This is done by multiplying each tile in matrix A by its respective tile in matrix B.
3. Result accumulation: Partial results are accumulated in the output matrix (also tiled) as they are calculated. These partial results are added to obtain the final resulting matrix.
![tmm-59dd890f48435e692c47919d0df4a5e6](https://github.com/Vicks0712/MatrixMultiplicationImplementations/assets/90756558/65aba0b4-3fe0-4e8e-a29b-0a36d387f185)


## Hadoop

The Hadoop distributed processing framework is used to distribute the work of matrix multiplication across a cluster of computers. This allows for increased speed and scalability in processing large matrices.

## Mapper-Reducer

The multiplication process is divided into two main steps. The Mapper is responsible for splitting matrices into submatrices and calculating partial products, while the Reducer sums these partial products to obtain the final result.

## Submatrices

The original matrices are divided into smaller submatrices, making manipulation and parallel processing more manageable. Each submatrix is multiplied individually, and the results are combined to obtain the complete output matrix.

## Key Points of the Code

### Module 1 (Hadoop)

This module handles the integration of Hadoop. The `Driver` class is the program's main entry point, configuring and executing Hadoop jobs. The Mapper and Reducer perform mapping and reducing operations for matrix multiplication.

### Module 2 (Matrix)

This module manages logic related to matrix manipulation. The `MatrixPartition` class represents a matrix partition and is used for extracting and setting values. The `Partitioner` class divides the original matrices into submatrices, and the `SubMatrixCreator` class creates these submatrices.

### Module 3 (Utils)

This module contains utility classes, such as `FileProccesor`, which is used to write submatrices to disk, and `MultiplicationManager`, which manages the multiplication of submatrices.

## Usage Instructions

To use this project, follow these steps:

1. Set up a Hadoop environment if you haven't already.

2. Execute the main program using the `Driver` class. Provide the following paths as arguments:

   - `<input_path>`: The location of the input matrices.
   - `<output_path>`: The location where the output matrix will be saved.
   - `<number_of_submatrices>`: The number of submatrices into which the original matrices will be divided.

   Ensure you provide valid input and output file paths, as well as the appropriate number of submatrices according to your needs.

The project will process the matrices and generate the resulting matrix at the specified output location.

## Contributions

Contributions to this project are highly encouraged and welcomed. If you wish to enhance the code, rectify errors, or introduce new features, please do not hesitate to submit a pull request.
