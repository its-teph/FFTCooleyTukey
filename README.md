# Parallel Fast Fourier Transform using Cooley Tukey Algorithm

Google Colab Link: https://colab.research.google.com/drive/16pGEHTBlHSDq4Yk-BA_LaDzZocQAbUZJ?usp=sharing


This project aims to implement Parallel Fast Fourier Transform (FFT) using Cooley-Tukey Algorithm in CUDA Programming. The CUDA implementation will be measured and compared to the C Language implementation of the same algorithm. The code will be implemented in Google Colab. 

The algorithm used in this project for the Implementation of Fast Fourier Transform is the Cooley-Tukey Algorithm, which is a widely used method for the implementation of FFT. This Cooley-Tukey algorithm has a time complexity of O(N log N), where N is the number of samples. This makes it significantly faster than the Discrete Fourier Transform (DFT) algorithm, which has a time complexity of O(N^2). By utilizing the divide-and-conquer approach, the Cooley-Tukey algorithm reduces the number of operations required to compute the FFT, making it highly efficient for large input sizes. 

