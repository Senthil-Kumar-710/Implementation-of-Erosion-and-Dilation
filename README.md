# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>

### Step2:
Create the text image using cv2.putText().
<br>

### Step3:
Create the structuring kernel for image dilation and erosion.
<br>

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.
<br>

### Step5:
Plot the images using plt.imshow().
<br>
<br>
<br>
 
## Program:

## Developed By: Senthil Kumar S
## Reg No: 212221230091

### Import the necessary packages
``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
```
### Create the Text using cv2.putText
```python
# Create the text using cv2.putText
text_img = np.zeros((100,250),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SCRIPT_COMPLEX
cv2.putText(text_img,"Senthil",(6,69),font,2,(255),2,cv2.LINE_AA) 
plt.title("Original Image")
plt.imshow(text_img,'Greens')
plt.axis('off')
```
### Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(4,4))
```
### Erode the image
```python
img_erode = cv2.erode(text_img,kernel)
plt.title("Eroded Image")
plt.imshow(img_erode,'Greens')
plt.axis('off')
```
### Dilate the image
```python
img_dilate = cv2.dilate(text_img,kernel)
plt.title("Dilated Image")
plt.imshow(img_dilate,'Greens')
plt.axis('off')
```
## Output:

### Display the input Image
![1](https://user-images.githubusercontent.com/93860256/235347310-0a6f9edd-115e-496f-9432-5522e833f924.png)
<br>

### Display the Eroded Image
![2](https://user-images.githubusercontent.com/93860256/235347313-48076b26-8703-46e5-a9bb-46d2022dc5c5.png)
<br>

### Dilated Image
![3](https://user-images.githubusercontent.com/93860256/235347315-1ca3ead2-a9c2-4592-88ec-78634ddcfe1f.png)
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
