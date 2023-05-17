# Implementation-of-Filters
## AIM:
To implement filters for smoothing and sharpening the images in the spatial domain.
## SOFTWARE REQUIRED:
Anaconda - Python 3.7
## ALGORITHM:
### Step 1:
Import the necessary modules. 
### Step 2:
For performing smoothing operation on a image. 
- Average filter
```python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
```
- Weighted average filter
```python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
```
- Gaussian Blur 
```python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
```
- Median filter
```python
median=cv2.medianBlur(image2,13)
```
### Step 3:
For performing sharpening on a image.
- Laplacian Kernel
```python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
```
- Laplacian Operator
```python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
```
### Step 4:
Display all the images with their respective filters.
## PROGRAM:
```python
# Developed By   : Jagadeeshreddy561
# Register Number: 212222240059

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("bts.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
### 1. Smoothing Filters
i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```
### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```
## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter

![ex61](https://user-images.githubusercontent.com/75235209/167778028-7381c43c-3430-47a4-a300-4a84ea0238c0.PNG)


ii) Using Weighted Averaging Filter

![exp62](https://user-images.githubusercontent.com/75235209/167778074-e54c6f9b-77d4-4716-ab91-5d6422c56721.PNG)



iii) Using Gaussian Filter

![exp63](https://user-images.githubusercontent.com/75235209/167778148-37767432-a727-43a3-84de-6d0ecc524e64.PNG)


iv) Using Median Filter

![exp64](https://user-images.githubusercontent.com/75235209/167778223-772c2a14-e51c-4ec3-9c7c-3f9f456a4ce5.PNG)



### 2. Sharpening Filters

i) Using Laplacian Kernal

![exp65](https://user-images.githubusercontent.com/75235209/167778277-a8350f0e-8b45-410c-af95-82429f83319d.PNG)



ii) Using Laplacian Operator

![exp66](https://user-images.githubusercontent.com/75235209/167778305-ab38d2ad-644d-49dc-8e17-77bd9fd6b291.PNG)



## RESULT:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
