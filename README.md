# OPENING--AND-CLOSING :
## Aim :
To implement Opening and Closing using Python and OpenCV.

## Software Required :
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText



### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program: 
### Developed by : MAMTHA I
### Reg no : 212222230076

``` Python
# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'ALBATROSS !',(5,70), font,2,(255),5,cv2.LINE_AA)

# Create the structuring element

kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Use Opening operation

image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")


# Use Closing Operation

image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")



```
## Output:

### Display the input Image :

![image](https://github.com/Mamthaiyappaprabu/OPENING--AND-CLOSING/assets/119393563/a1eb62cc-8ee6-4b7c-8735-68b3a92895a4)



### Display the result of Opening :
![image](https://github.com/Mamthaiyappaprabu/OPENING--AND-CLOSING/assets/119393563/3abb4f4a-9c5a-4ddf-bec2-67dc805c6076)



### Display the result of Closing :

![image](https://github.com/Mamthaiyappaprabu/OPENING--AND-CLOSING/assets/119393563/2a5b6935-d63f-414e-a865-15e0e763fea6)



## Result :
Thus the Opening and Closing operation is used in the image using python and OpenCV.
