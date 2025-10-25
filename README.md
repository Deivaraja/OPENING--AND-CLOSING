
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:

Create the structuring element.
### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:
### DEVELOPED BY: DEIVARAJA R
### REGISTER NO: 212224240031

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'DEIVARAJA R', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```
## Output:

### Display the input Image

<img width="1022" height="167" alt="image" src="https://github.com/user-attachments/assets/80d9e5c6-56fe-455a-8921-03573f7b9aa4" />


### Display the result of Opening
<img width="976" height="165" alt="image" src="https://github.com/user-attachments/assets/4dd57beb-c7fa-4cfd-ab89-94b1bd3f391d" />




### Display the result of Closing
<img width="1058" height="192" alt="image" src="https://github.com/user-attachments/assets/b0fcdebf-7306-49bb-a22a-ae5856523756" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
