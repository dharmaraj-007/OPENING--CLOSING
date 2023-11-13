# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>
### Step2:
Create the Text using cv2.putText.
<br>
### Step3:
Create the structuring element.
<br>
### Step4:
Use Opening operation
<br>
### Step5:
Use Closing Operation
<br>
## Program:
```
Developed by : DHARMARAJ S
Register Number:212222240025
```

# Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
``` Python
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(img1,'DHARMARAJ S',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Create the structuring element
``` Python
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
``` Python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('OPENING'), plt.xticks([]), plt.yticks([])
plt.show()
```

# Use Closing Operation

``` Python
image1=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('CLOSING'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:

### Display the input Image

![1](https://github.com/dharmaraj-007/OPENING--CLOSING/assets/119560386/c0c58ba6-0a92-47c0-b5f6-afd64dd887f8)

### Display the result of Opening

![2](https://github.com/dharmaraj-007/OPENING--CLOSING/assets/119560386/e15d02be-6801-4bd0-ab71-6a10164b2c79)

### Display the result of Closing

![Screenshot 2023-11-13 171001](https://github.com/dharmaraj-007/OPENING--CLOSING/assets/119560386/efe52346-fbcd-4a6f-a4fb-86a2fc477a04)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
