# Sobel-operator-Edge-Detection
A simple Edge Detection using the Sobel operator

## Application

The Sobel Operator help us get the edges of an image by computing an aproximation of an image gradient. At each point the result is either the corresponding gradient vector or the norm of this vector.

By convoluting our image with our first kernel from left to right we get the Gradient in the X direction

![Gradient_in_x](https://latex.codecogs.com/gif.latex?G_%7Bx%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%20&plus;1%20%26%200%20%26%20-1%5C%5C%20&plus;2%20%26%200%20%26%20-2%5C%5C%20&plus;1%20%26%200%20%26%20-1%20%5Cend%7Bbmatrix%7D)

Then by convoluting our image with our first kernel from top to bottom we get the Gradient in the Y direction

![Gradient in y](https://latex.codecogs.com/gif.latex?G_%7By%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%20&plus;1%20%26%20&plus;2%20%26%20&plus;1%5C%5C%200%20%26%200%20%26%200%5C%5C%20-1%20%26%20-2%20%26%20-1%20%5Cend%7Bbmatrix%7D)

At this point we have the vectors of the gradient of the image. Now by finding the magnitude o each vector we will get the edges we need.

![Gradient Magnitude](https://latex.codecogs.com/gif.latex?G%20%3D%20%5Csqrt%7B%28G_%7Bx%7D%29%5E%7B2%7D%20&plus;%20%28G_%7By%7D%29%5E%7B2%7D%7D)
