# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
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

```

# Developed By: HAREESH R
# Register No: 212223230068

import cv2
import numpy as np
import matplotlib.pyplot as plt
#i) Create the Text using cv2.putText
img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"HAREESH R",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()
#ii) Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
#iii) Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()
#iv) Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:
 
### Display the input Image

![Screenshot 2025-05-06 094607](https://github.com/user-attachments/assets/79688e0d-985d-4b87-b1fa-498c32c28c57)

### Display the result of Opening

![Screenshot 2025-05-06 094623](https://github.com/user-attachments/assets/f39c566a-a670-46a2-8476-3e1a8509cddb)


### Display the result of Closing


![Screenshot 2025-05-06 094633](https://github.com/user-attachments/assets/a1282c57-f1b9-4e3c-adf1-2467d163f523)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
