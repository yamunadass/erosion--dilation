# EX-09:Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:Initialize an Empty Image:

Create a black image of size 100x600 pixels.
### Step-2:Add Text to the Image:

Use a specified font to write the word "Lifestyle" on the image at a defined position.
### Step-3:Display the Original Image:

Show the image containing the text without axis labels.
### Step-4:Create Structuring Elements:

Define a structuring element for morphological operations (e.g., a cross-shaped kernel).
### Step-5:Erode the Image:

Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### Step-6:Dilate the Image:

Apply dilation to the original image using the same structuring element to increase the size of white regions.

 
# Program:

#### Developed By: Yamuna M
#### Reference Number : 212223230248

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
cv2.putText(img ,'Lifestyle',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/064fa4b0-dcf6-4f3a-aef1-5dfa0d972f43)

# Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
![alt text](image-1.png)
# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/486ae98d-5fd4-4e54-a3ce-1bd1af19ce45)


# Dilate the image

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/b9915a5c-ac30-43a2-8e26-7b6db58b6713)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
