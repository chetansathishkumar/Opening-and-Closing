## EX.NO: 11 <br>
## DATE: 17.05.2023
## <p align="center">OPENING AND CLOSING</p>


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
Use Opening and Closing Operations
<br>

### Step5:
End Program.
<br>

## Program:
```
DEVELOPED BY: P S Chetan
REG NO: 212220230033
```

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,500),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Chetan",(5,70),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image

![image](https://user-images.githubusercontent.com/75260837/171335227-27ea4552-c8d9-444e-9849-3e2dce2cafce.png)


### Display the result of Opening

![image](https://user-images.githubusercontent.com/75260837/171335634-edc09695-e195-42ce-bc2d-7dda63a70b90.png)


### Display the result of Closing

![image](https://user-images.githubusercontent.com/75260837/171335706-38d02627-f1ba-45e3-92cd-1ebeb4a53cd0.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
