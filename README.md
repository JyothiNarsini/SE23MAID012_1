# Matrix Multiplication with OpenMP

## Code Explanation

This program performs the following steps:

1. **Command-Line Arguments**: It accepts two command-line arguments - `matrix_size` and `num_threads`. These arguments determine the size of the matrices and the number of threads to use for parallel execution.

2. **Memory Allocation**: Dynamic memory allocation is used to create three matrices `A`, `B`, and `C`. These matrices will hold the input matrices and the result of matrix multiplication.

3. **Initialization**: Matrices `A` and `B` are initialized with the value 2, while matrix `C` is initialized with zeros.

4. **Parallel Matrix Multiplication**: The core matrix multiplication operation is parallelized using OpenMP. The `#pragma omp parallel for` directive splits the work among multiple threads. Each thread calculates a portion of the result matrix `C`.

5. **Timing**: The program measures the elapsed time for the matrix multiplication using the `gettimeofday` function. This provides a measure of the program's performance.

6. **Memory Deallocation**: After the matrix multiplication is complete, memory is deallocated to prevent memory leaks.

## How to Compile and Run

To compile the program, open a terminal and navigate to the directory containing the code. Use the following command:

```bash
gcc -o matrix_multiplication matrix_multiplication.c -fopenmp
```

This command compiles the code with OpenMP support and generates an executable named matrix_multiplication.

To run the program, use the following command:
```bash
./matrix_multiplication <matrix_size> <num_threads>
```

For finding nth power of the matrix:
```bash
./matrix_multiplication <matrix_size> <exponent> <num_threads>
```

Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2
```

For nth power:
Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2 4
```

This will perform matrix multiplication with matrices of size 1000x1000 using 4 threads.

## Output

The program will display the size of the matrices, the number of threads used, and the elapsed time for matrix multiplication.

Graph for the same are as below:

1. **OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/56303c8b-eea4-407b-923c-96728379e38a)

     ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/63ac6051-ac9b-4e84-b542-c307cf13966a)

     ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/ced8ea4e-8724-46b2-ad0e-ac1656ecbbc4)


   
2. **Nth Power of Matrix with OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/ecc709d7-c9c4-4042-98d0-e591ba1d06f5)

     ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/4726faf3-74e4-4bdd-b524-143f080f1058)

     ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/65ca02cb-d90e-4a9e-a091-43ad106d3e3f)

   

## Conclusion

This C program demonstrates how to use OpenMP to parallelize matrix multiplication, improving the performance of the computation. You can adjust the matrix size and the number of threads to observe the impact on execution time.




# Block Matrix Multiplication

```markdown
# Block Matrix Multiplication

Compile the program using a C compiler. For example:

gcc -o block_matrix_mult block_matrix_mult.c -fopenmp
```

Here, block_matrix_mult is the name of the executable.

To run the program, use the following command-line format:
```bash
./block_matrix_mult <matrix_size> <num_threads> <block_size>
```

For nth power of a matrix using BMM:
```bash
./block_matrix_mult <matrix_size> <exponent> <num_threads> <block_size>
```

<matrix_size>: The size of the square matrices (e.g., 100 for a 100x100 matrix).
<block_size>: The size of the square blocks (e.g., 10 for a 10x10 block).
For example, to multiply two 100x100 matrices using 10x10 blocks:

```bash
./block_matrix_mult 1024 6 4
```

For nth power:
```bash
./block_matrix_mult 1024 2 6 4
```

## Output
The program will display the size of the matrices, the block size, and the result of the multiplication.

1. **BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/652f6bd7-5339-4ff2-826c-1c034e59d5bf)


   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/f73b6c96-3b1d-413e-990e-fa77e69527e1)


   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/eeca62a8-8960-43ea-98b3-8c32d8756385)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/9830571a-ccd8-424f-9332-bbab479c3a30)


   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/14d81ae9-cd5e-478f-bd0d-35ee39e35ae3)


   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/630d27de-fe84-4004-95d5-009e7cd374bb)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/2ea630a8-09e9-4710-bcda-f784f23770be)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/4ed465e9-c2de-4d51-b0b7-890507176fc0)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/d025cca8-2ba1-4bf1-b139-a41797fffe7f)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/20d71251-0b6b-4fd9-b5eb-a22c99848018)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/6debdb8f-6edc-47ae-a296-1a55764c2cab)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/1d84bf3e-f49d-4844-859c-ad58b0bf44e0)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/8cedbfb5-54a4-4a24-acb4-57a682130733)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/32d74c9d-dc57-484c-9cfe-49a996b75de2)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/a11d5348-a9d8-4eac-8c59-b487b5d18978)

   
3. **Nth Power of Matrix with BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/0342a33b-71e7-46d8-8ad8-b9e0a5d1f00b)

   ![image](https://github.com/JyothiNarsini/SE23MAID012_1/assets/88646255/9f788282-7e9a-496a-8194-743cd2d04853)


## Memory Management
The program dynamically allocates memory for matrices A, B, and C, as well as for the block buffers. It frees the allocated memory after the multiplication is complete to prevent memory leaks.
