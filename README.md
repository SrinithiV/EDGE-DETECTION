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

## PROGRAM :
### DEVELOPED BY : SRINITHII V
### REGISTER NO. : 212222110046
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('harry.jpg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.figure(figsize=(7,3))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
#### OUTPUT:
![Screenshot 2024-10-26 110832](https://github.com/user-attachments/assets/9fc432ab-b87d-405f-9dc9-86d7f404137a)

### SOBEL EDGE DETECTOR
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.figure(figsize=(7,3))
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
#### OUTPUT
![Screenshot 2024-10-26 110841](https://github.com/user-attachments/assets/4d9c807e-d9cc-43bc-bc5d-6108999795e4)

### LAPLACIAN EDGE DETECTOR
```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.figure(figsize=(7,3))
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
#### OUTPUT:
![Screenshot 2024-10-26 110851](https://github.com/user-attachments/assets/ac9a6baa-7b11-4d76-9d8b-890ce3ce0552)

### CANNY EDGE DETECTOR
```python
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.figure(figsize=(7,3))
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
#### OUTPUT:
![Screenshot 2024-10-26 110900](https://github.com/user-attachments/assets/4d491ada-b8ca-4e1d-908a-5f9a2e7e6402)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
