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
text_img = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SCRIPT_COMPLEX
cv2.putText(text_img,"Senthil Kumar",(6,69),font,2,(255),2,cv2.LINE_AA) 
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
![1](https://github.com/Senthil-Kumar-710/demo/assets/93860256/e2a01462-24f9-4721-ae8e-6a4b0cd8c5c2)
<br>

### Display the Eroded Image
![2](https://github.com/Senthil-Kumar-710/demo/assets/93860256/4500ee3d-e7f2-43e9-a6d3-d0782533f2e4)
<br>

### Dilated Image
![3](https://github.com/Senthil-Kumar-710/demo/assets/93860256/34b62427-13c8-4f6d-aa7c-5bd21c3d191b)
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
