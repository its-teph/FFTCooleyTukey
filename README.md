# Parallel Fast Fourier Transform using Cooley Tukey Algorithm

Group 1:
CAI, Edison &
SUSADA, Stephanie Joy

Video Demo Link: https://drive.google.com/file/d/11Vyod_2Il_ucML5EPUw7sHimpy5XW5tH/view?usp=sharing

Google Colab Link: https://colab.research.google.com/drive/16pGEHTBlHSDq4Yk-BA_LaDzZocQAbUZJ?usp=sharing


This project aims to implement Parallel Fast Fourier Transform (FFT) using Cooley-Tukey Algorithm in CUDA Programming. The CUDA implementation will be measured and compared to the C Language implementation of the same algorithm. The code will be implemented in Google Colab. 

The algorithm used in this project for the Implementation of Fast Fourier Transform is the Cooley-Tukey Algorithm, which is a widely used method for the implementation of FFT. This Cooley-Tukey algorithm has a time complexity of O(N log N), where N is the number of samples. This makes it significantly faster than the Discrete Fourier Transform (DFT) algorithm, which has a time complexity of O(N^2). By utilizing the divide-and-conquer approach, the Cooley-Tukey algorithm reduces the number of operations required to compute the FFT, making it highly efficient for large input sizes. 

The pseudocode for the Cooley Tukey Algorithm is can be written as:

![image](https://github.com/its-teph/FFTCooleyTukey/assets/80933795/7ba754c0-ad7a-431a-8221-298d65262c2b)

## Parallel Algorithm Implemented


This final project is an implementation of the Fast Fourier Transform (FFT) algorithm using CUDA, which is designed to perform efficient calculations of the Discrete Fourier Transform (DFT) of a complex input sequence. The parallel algorithm implemented in the provided code is the Cooley-Tukey radix-2 Decimation in Time (DIT) Fast Fourier Transform (FFT) algorithm.

The program implementation for this project first sets up the necessary structures and memory on the GPU. It then defines a kernel function fft that performs the FFT calculations, distributing the workload among multiple threads and blocks to achieve parallelism. The main function initializes a complex input array and executes the FFT algorithm through a series of loops. After the FFT computations, it checks for errors by comparing the calculated FFT output with the original input. The code employs CUDA's memory management functions and synchronization mechanisms with grid stride loop for efficient GPU computation. 

## Execution Time Comparison - Sequential VS Parallel

The average execution time of the Sequential and Parallel implementation are compared with 30 runs each cases. 

| Array Size   | 2^8            | 2^20          | 2^24        | 2^26       |
|--------------|----------------|---------------|-------------|------------|
| Sequential   | 83.37us        | 549518.13us   | 1703862.30us|7671967.90us|
| Parallel     | 4.79us         | 700.27us      | 4239.1us    |11694us     |


The presented analysis contrasts two distinct implementations of the Fast Fourier Transform (FFT) algorithm: a Parallel FFT Cooley Tukey Implementation and a Sequential Implementation in the C programming language. The comparison centers around the evaluation of their respective execution times across various input sizes with 30 runs each test cases. The findings underscore a marked superiority of the Parallel FFT Cooley Tukey Implementation over its Sequential counterpart across all test cases.

Focusing on a specific input size, by the case where the input size is 2^8 (256), the distinction in average execution time between the two implementations is relatively large. Here, the Parallel Implementation achieves an execution time reduction of approximately 94.03%.
When considering an input size of 2^20, the Parallel Implementation showcases an exceptional execution time reduction of 99.87%. This enhancement in execution time signifies a substantial advancement in computational efficiency and resource utilization. Similarly, for an input size of 2^24, the parallel implementation yields a substantial execution time reduction of 99.5163%. It is worth noting that the program attains its upper limit in handling input sizes with 2^26 values, reflecting the extent of its computational capability. In this case, the Parallel implementation shows an execution time reduction of 95.5%. 

For the error checking, it's important to note that the data precision of the 'double' data type is constrained to around 15 decimal places. This limitation becomes apparent when working with significantly large values, as the precision diminishes with increasing magnitude. To address this concern, the group employed an error checking mechanism by comparing the differences between the values obtained after scaling down the post-4 FFT calculation and the original input values. The objective was to ascertain the accuracy of the computed FFT results. In the best-case scenario, the discrepancy between these values should ideally be less than 0.00000000000001. However, recognizing the diminishing precision, particularly with larger values, the group adopted a slightly more lenient threshold of 0.0000001 to facilitate error checking. This adjustment aims to strike a balance between precision and practicality, ensuring that the error checking process remains effective even when dealing with larger datasets and potential precision limitations.

## Conclusion

In computational algorithms, this analysis has delved into the efficiency of two Fast Fourier Transform (FFT) implementations using Cooley Tukey Algorithm: the Parallel Implementation in CUDA and the Sequential Implementation in C. The evaluation has been guided by the execution time, and the results shows Parallel FFT Cooley Tukey method consistently outperforms its Sequential counterpart.

Across a range of scenarios, the Parallel approach demonstrates a consistent advantage over the Sequential method, showcasing superior computational speed and resource management. Notably, this advantage becomes more pronounced with larger input sizes. For instance, at an input size of 2^8 (256), the Parallel approach achieves a 94.03% reduction in execution time. Scaling up to 2^20, the gain is substantial, with an impressive 99.87% reduction in execution time. Similarly, at an input size of 2^24, the Parallel approach achieves a significant execution time reduction of 99.5163%.

It's worth noting that the program's capabilities have limitations, comfortably handling inputs up to 2^26 values. This milestone underscores the proficiency of the implementation while also highlighting the constraints inherent in parallel processing.

In summary, the Parallel FFT Cooley Tukey Implementation in CUDA emerges as a beacon of efficiency, offering substantial performance improvements in FFT calculations. Given the evident advantages showcased by the Parallel FFT Cooley Tukey Implementation in CUDA in terms of computational efficiency and substantial execution time reduction, the group highly recommended to consider its application in the realm of audio processing. Unfortunately, the group was not able to implement this in real audio data and was not able to make a audio compressor out of Parallel FFT using Cooley-Tukey Algorithm. While the group may have encountered limitations in terms of time and resources, leveraging parallel computing techniques like the Parallel FFT can significantly enhance the processing capabilities for audio processing with larger datas without needing a large amount of computer resources.
