# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using a function warpPerpective()

### Step3:
Scale the image by multiplying the rows and columns with a float value.

### Step4:
Shear the image in both the rows and columns.

### Step5:
Find the reflection of the image.

## Program:
```python
Developed By: S.Shanmathi
Register Number: 212222100049


import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("pic.jpg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape

i)Image Translation

M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()

ii) Image Scaling

plt.imshow(input_image)
plt.show()
rows,cols,dim = input_image.shape
M = np.float32([[1.5,0,0],
                [0,1.7,0],
                [0,0,1]])
scaled_img = cv2.warpPerspective(input_image,M,(cols*5,rows*5))
plt.imshow(input_image)
plt.show()

iii)Image shearing

plt.axis('off')
plt.imshow(input_image)
plt.show()
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(input_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(input_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()

iv)Image Reflection

M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(input_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(input_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()

v)Image Rotation

rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping

plt.imshow(input_image)
plt.show()
cropped_img=input_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()

```
## Output:

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/648ec995-5f14-4887-91b5-bc68e952b39b)

### i)Image Translation

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/41eb8c8b-59ea-4f63-a003-85c0bc7b5d49)

### ii) Image Scaling

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/7cf3882c-bb40-424d-89b7-90bfa504480a)

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/7c8383cf-fdf1-4e37-ab39-c215fc0c81c2)

### iii)Image shearing

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/9eca1e7e-07ce-4ecb-a259-9275108ecb9c)

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/418b3e7a-8b60-478f-a15b-9e24a7be1c70)

### iv)Image Reflection

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/db63cb71-c8c3-4c3c-a6ab-2de5765483d4)

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/9feac06a-9fcb-40a0-ad13-7fb88dab71bd)

### v)Image Rotation

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/2bcfca01-0f05-4e39-ade3-804ece14bf56)

### vi)Image Cropping

![image](https://github.com/ShanmathiShanmugam/IMAGE-TRANSFORMATIONS/assets/121243595/90844e04-5efe-4128-959f-81848116510d)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
