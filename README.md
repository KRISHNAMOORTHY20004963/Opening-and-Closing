# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring element for opening and closing.

### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step5:
Show the images using cv2.imshow().
 
## Program:
```
/*
Developed by   : Krishna moorthy S
Register Number: 212220230025
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,800),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Krishna Moorthy S",(5,70),font,3,(255,0,0),5,cv2.LINE_AA)
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
![xc2]![dip 1](https://user-images.githubusercontent.com/75241177/172300618-ab0fdd80-a32d-4e90-9ed2-568b614c8c5f.jpg)

### Display the result of Opening
![xc2]![dip2](https://user-images.githubusercontent.com/75241177/172300709-24a50c42-5a7e-4298-a25d-4fd529908f56.jpg)

### Display the result of Closing
![xc3]![dip 3](https://user-images.githubusercontent.com/75241177/172300753-c96d8a0e-200c-4052-b77d-e7799b48ccaf.jpg)




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
