# Parallel Fast Fourier Transform using Cooley Tukey Algorithm

Google Colab Link: https://colab.research.google.com/drive/16pGEHTBlHSDq4Yk-BA_LaDzZocQAbUZJ?usp=sharing


This project aims to implement Parallel Fast Fourier Transform (FFT) using Cooley-Tukey Algorithm in CUDA Programming. The CUDA implementation will be measured and compared to the C Language implementation of the same algorithm. The code will be implemented in Google Colab. 

The algorithm used in this project for the Implementation of Fast Fourier Transform is the Cooley-Tukey Algorithm, which is a widely used method for the implementation of FFT. This Cooley-Tukey algorithm has a time complexity of O(N log N), where N is the number of samples. This makes it significantly faster than the Discrete Fourier Transform (DFT) algorithm, which has a time complexity of O(N^2). By utilizing the divide-and-conquer approach, the Cooley-Tukey algorithm reduces the number of operations required to compute the FFT, making it highly efficient for large input sizes. 

The pseudocode for the Cooley Tukey Algorithm is can be written as:

![image](https://github.com/its-teph/FFTCooleyTukey/assets/80933795/7ba754c0-ad7a-431a-8221-298d65262c2b)

## Parallel Algorithm Implemented


This final project is an implementation of the Fast Fourier Transform (FFT) algorithm using CUDA, which is designed to perform efficient calculations of the Discrete Fourier Transform (DFT) of a complex input sequence.

The program implementation for this project first sets up the necessary structures and memory on the GPU. It then defines a kernel function fft that performs the FFT calculations, distributing the workload among multiple threads and blocks to achieve parallelism. The main function initializes a complex input array and executes the FFT algorithm through a series of loops. After the FFT computations, it checks for errors by comparing the calculated FFT output with the original input. The code employs CUDA's memory management functions and synchronization mechanisms with grid stride loop for efficient GPU computation. 

## Execution Time Comparison - Sequential VS Parallel

| Array Size | 2^20 | 2^24 |
| :---         |     :---:      |     :---:     |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
