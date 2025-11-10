# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Import required libraries.

### Step2:
Read the image and convert it to grayscale then display it.

### Step3:
Use Global thresholding to segment the image

### Step4:
Use Adaptive thresholding to segment the image

### Step5:
Use Otsu's method to segment the image 

### Step6:
End the program.

## Program

## DEVELOPED BY : SUBHASHRI R
## REG NO : 212223230219

```

# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read the Image and convert to grayscale
image = cv2.imread('ironman.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Use Global thresholding to segment the image
ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

# Use Adaptive thresholding to segment the image
th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY, 11, 2)

# Use Otsu's method to segment the image 
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)


# Display the results

plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()

plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()

plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()

```
## Output

### Original Image

<img width="688" height="474" alt="image" src="https://github.com/user-attachments/assets/39f1f06d-c7a8-4e57-b1f1-ad4c71705797" />


### Global Thresholding

<img width="623" height="417" alt="image" src="https://github.com/user-attachments/assets/3f4d8449-4b8c-41e8-980e-660a3d18cf73" />



### Adaptive Thresholding

<img width="655" height="420" alt="image" src="https://github.com/user-attachments/assets/a63b1989-d88f-407a-b27f-4ba96e85c76e" />




### Optimum Global Thesholding using Otsu's Method

<img width="632" height="423" alt="image" src="https://github.com/user-attachments/assets/e60505fd-a2de-438b-b30c-da6cbc6f48a6" />




## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
