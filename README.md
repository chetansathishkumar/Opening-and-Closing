# Opening-and-Closing

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

![Screenshot 2022-05-31 144706](https://user-images.githubusercontent.com/75235212/171139922-8306e845-4a2b-473e-8dea-1ebb14ad6abd.png)


### Display the result of Opening

![Screenshot 2022-05-31 144832](https://user-images.githubusercontent.com/75235212/171139931-333d9399-a462-47e6-baa8-66a5d6dca139.png)


### Display the result of Closing

![Screenshot 2022-05-31 144915](https://user-images.githubusercontent.com/75235212/171139947-9a82bd0d-769f-4658-a2ce-13f9b5c00c9d.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
