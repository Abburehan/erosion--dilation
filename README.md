# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Program:
### Developed by : SYED ABBU REHAN
### Register Number : 212223240165
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'REHAN',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')


# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
## Output:

### Display the input Image
![image](https://github.com/Abburehan/erosion--dilation/assets/138849336/3745627f-1270-459d-a2d6-5c475e1299ba)

### Display the Eroded Image
![image](https://github.com/Abburehan/erosion--dilation/assets/138849336/702590da-0373-4207-adf6-66ad81df0e4d)

### Display the Dilated Image
![image](https://github.com/Abburehan/erosion--dilation/assets/138849336/559ee6de-56b4-47f2-b838-e33663a1f2b9)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
