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
cv2.putText(img, 'MOUNIKA', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11)
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
<br>
<br>
<br>
<img width="733" height="193" alt="image" src="https://github.com/user-attachments/assets/7646c296-1a3b-4618-9e2b-0ae1cad151db" />

<br>
<br>
<br>

### Display the result of Opening
<br>
<br>
<br>
 <img width="798" height="228" alt="image" src="https://github.com/user-attachments/assets/55c196f7-92f0-419f-94c8-43c1a8af9ab0" />

<br>
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>
<img width="775" height="276" alt="image" src="https://github.com/user-attachments/assets/1c56eb35-3027-47a5-902f-d6097632ef45" />

<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
