# Implementation-of-filter
## NAME:PAVITHRAN S
## REG NO:212223240113
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>

Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 


## Program:
### Developed By   :
### Register Number:
</br>

### 1. Smoothing Filters

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("nature.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
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
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```
## OUTPUT:
### 1. Smoothing Filters

<img width="380" height="276" alt="image" src="https://github.com/user-attachments/assets/a52865a5-4285-4c3d-8528-ede06975096d" />


i) Using Averaging Filter

<img width="380" height="276" alt="image" src="https://github.com/user-attachments/assets/a9dc3bb4-5042-4ca9-881d-05455eaa2198" />


ii)Using Weighted Averaging Filter

<img width="637" height="456" alt="image" src="https://github.com/user-attachments/assets/542bc744-0d83-44e8-bfcc-1bb95c67b6ae" />

iii)Using Gaussian Filter

<img width="642" height="460" alt="image" src="https://github.com/user-attachments/assets/42358909-ca04-41d1-ba05-bab90721b3cc" />

iv) Using Median Filter

<img width="645" height="463" alt="image" src="https://github.com/user-attachments/assets/77299f92-de6a-4085-8cc6-e3c061b123e6" />

### 2. Sharpening Filters

i) Using Laplacian Kernal

<img width="649" height="474" alt="image" src="https://github.com/user-attachments/assets/dddaa51f-a3ae-46ef-a7ca-2dc79489d272" />

ii) Using Laplacian Operator


<img width="642" height="462" alt="image" src="https://github.com/user-attachments/assets/5f0cc91a-d186-419c-afdb-264e4fb84995" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
