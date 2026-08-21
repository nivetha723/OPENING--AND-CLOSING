# OPENING--AND-CLOSING
## Name:Nivetha N
## Reg.no:212225040290
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

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((500, 500, 3), dtype=np.uint8)

font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Open and Close', (100, 250), font, 1,
            (255, 255, 255), 2, cv2.LINE_AA)

kernel = np.ones((3, 3), np.uint8)

# Opening Operation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Closing Operation
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# Display images
plt.figure(figsize=(12, 4))

plt.subplot(1, 3, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image")
plt.axis('off')

plt.subplot(1, 3, 2)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))
plt.title("Opening Operation")
plt.axis('off')

plt.subplot(1, 3, 3)
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))
plt.title("Closing Operation")
plt.axis('off')

plt.show()







```
## Output:

### Display the input Image
<img width="301" height="232" alt="image" src="https://github.com/user-attachments/assets/d3065d53-fd54-4adc-a5ca-26992aaa41da" />

### Display the result of Opening
<img width="223" height="226" alt="image" src="https://github.com/user-attachments/assets/750614d3-234a-412e-8f28-f8fabc502740" />

### Display the result of Closing
<img width="238" height="247" alt="image" src="https://github.com/user-attachments/assets/59bfc8bf-7226-4ad2-9822-6a06fde49a58" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
