# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program:
### Original:
~~~
Developed by : Dhanusya K
Register no: 212223230043
~~~
~~~
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread("C:/Users/admin/Downloads/Digital images/ex_6_image.jpg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

~~~
### SOBEL EDGE DETECTOR
~~~
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
~~~
### LAPLACIAN EDGE DETECTOR
~~~
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
~~~
### CANNY EDGE DETECTOR
~~~
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
~~~

## Output:
### Original:
![436914839-5b4448f4-e2ce-41b8-a76f-66ea2d42335c](https://github.com/user-attachments/assets/94cca1fc-9153-4113-8fd9-d11c0542e1f6)

### SOBEL EDGE DETECTOR

![436914995-d126359e-42e2-41a1-8422-cf8fa6ebb5cb](https://github.com/user-attachments/assets/275eb4ce-3f09-40f2-aaf8-3b8f32128163)


### LAPLACIAN EDGE DETECTOR
![436915765-9a9e96fc-1f8d-4d0f-9e96-c4506a7e6278](https://github.com/user-attachments/assets/ba414bf7-4e3e-4d0e-8025-b34da77afe2c)



### CANNY EDGE DETECTOR
![436915803-f6565d42-ef7b-4623-a8fd-edf33333c2a9](https://github.com/user-attachments/assets/4a71e326-50ea-4dd3-bfe4-2f8775aa18d2)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
