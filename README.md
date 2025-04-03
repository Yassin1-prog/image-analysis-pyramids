# Image Pyramids in Python: Gaussian and Laplacian Implementation

This notebook implements Gaussian and Laplacian pyramids for image analysis, following the concepts described in the paper "The Laplacian Pyramid as a Compact Image Code" by Burt, P. J. and Adelson, E. H.

This project leverages the power of NumPy for numerical operations, OpenCV for image processing, and Matplotlib for visualization.

## Notebook Contents

**1. Theoretical Background:**

* Brief answers to theoretical questions based on the Burt and Adelson paper, covering:
    * The effect of the parameter 'a' on the Gaussian pyramid.
    * The definition of entropy and the maximum entropy of a grayscale image.
    * The impact of bin size on quantization.
    * The influence of the number of pyramid levels on quantization.

**2. Algorithm Implementation:**

* Implementation of the following functions for image pyramid generation and manipulation:
    * `GKernel(a)`: Creates a Generating Kernel based on parameter 'a'.
    * `GREDUCE(I, h)`: Reduces an image according to the Generating Kernel.
    * `GPyramid(I, a, depth)`: Generates and stores a Gaussian pyramid for a given image, 'a', and depth.
    * `GEXPAND(I, h)`: Expands an image according to the Generating Kernel.
    * `LPyramid(I, a, depth)`: Generates the Laplacian pyramid of an image using the Gaussian pyramid.
    * `L_Pyramid_Decode(L, a)`: Decodes a Laplacian pyramid to reconstruct the image.
    * `L_Quantization`: Implements quantization of the Laplacian pyramid.

**3. Algorithm Testing:**

* Testing of the implemented `L_Pyramid` and `L_Pyramid_Decode` functions using the 'Lena' and 'camera' images (supporting both color and grayscale).
* Visualization of the original and reconstructed images using different values of 'a' (ranging from 0.3 to 0.7).
* Visualization of the original and reconstructed images using different pyramid depths (ranging from 3 to 6).
* Calculation and presentation of entropy for different values of 'a' and 'depth' for both test images, along with corresponding analysis.
* Identification of the optimal 'a' value (with respect to entropy) at each level of the Laplacian pyramid for both test images.
* Quantization of the 'Lena' and 'camera' images using the optimal 'a' value and different bin sizes (two experiments per image).

