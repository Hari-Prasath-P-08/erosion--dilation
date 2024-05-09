# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
### Developed by : Hari Prasath. P
### Reg no : 212223230070

# Import the necessary packages

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText

```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'POWER',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```

# Create the structuring element

```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```

# Erode the image

```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```

# Dilate the image

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```

## Output:

### Display the input Image

![Screenshot 2024-05-09 080148](https://github.com/Hari-Prasath-P-08/erosion--dilation/assets/139455593/63c44031-cd48-464d-a22a-728c82ed000f)

### Display the Eroded Image

![Screenshot 2024-05-09 080156](https://github.com/Hari-Prasath-P-08/erosion--dilation/assets/139455593/b2870d02-17c9-4266-a9c5-650b5d573a23)

### Display the Dilated Image

![Screenshot 2024-05-09 080202](https://github.com/Hari-Prasath-P-08/erosion--dilation/assets/139455593/f9dfb452-e51a-4b14-9780-338b55e8cf57)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
