# EX-09:Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:

Create a black image of size 100x600 pixels.
### Step-2:

Use a specified font to write the word "Lifestyle" on the image at a defined position.
### Step-3:

Show the image containing the text without axis labels.
### Step-4:

Define a structuring element for morphological operations (e.g., a cross-shaped kernel).
### Step-5:

Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### Step-6:

Apply dilation to the original image using the same structuring element to increase the size of white regions.

## Program:
```
Developed By: Yamuna M
Reference Number :212223230248
``` 
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'YAMUNA',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
![Screenshot 2024-10-16 110144](https://github.com/user-attachments/assets/eee77bf4-7407-4ab9-b10f-762b7170be5c)


# Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
![Screenshot 2024-10-16 110153](https://github.com/user-attachments/assets/f9f1991e-6823-4406-8670-1a0c8739b2e0)


# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
![Screenshot 2024-10-16 110203](https://github.com/user-attachments/assets/853b239b-3849-472d-8231-1ad1e4893308)


# Dilate the image

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
![Screenshot 2024-10-16 110210](https://github.com/user-attachments/assets/3b47b9ff-19f7-4b0f-b923-a3a5766e720e)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
