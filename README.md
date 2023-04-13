# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the required libraries and read the original image.
## Step2:
Translate the image.
## Step3:
Scale the image.
## Step4:
Shear the image.
## Step5:
Find reflection of image.
## Step6:
Rotate the image.
## Step7:
Crop the image.
## Step8:
Display all the Transformed images.

## Program:
```python
Developed By:Nivetha M
Register Number:212221240034
import cv2
import matplotlib.pyplot as plt
I = cv2.imread("unicon.jpeg")
I = cv2.cvtColor(I,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.axis('off')
plt.imshow(I)
plt.show()
i)Image Translation

rows,cols,dim = I.shape
import numpy as np
N = np.float32([[1,0,100],
                [0,1.9,200],
                [0,0,1]])
translated_image = cv2.warpPerspective(I,N,(cols,rows))
plt.imshow(translated_image)

ii) Image Scaling

rows,cols,dim = I.shape
N = np.float32([[2,0,0],
               [0,3,0],
               [0,0,1]])
               scaled_img = cv2.warpPerspective(I,N,(cols*2,rows*2))
plt.imshow(scaled_img)

iii)Image shearing

M_xy = np.float32([[1,0.5,0],
                   [0.5,1,0],
                   [0,0,1]])
shearedimage_xyaxis = cv2.warpPerspective(I,M_xy,(int(cols*1.5),int(rows*1.5)))
plt.imshow(shearedimage_xyaxis)

iv)Image Reflection

rows,cols,dim = I.shape
R_xy = np.float32([[1,0,cols],
                [0,-1,rows],
                [0,0,1]])
reflected_image_xyaxis = cv2.warpPerspective(I,M_xy,(int(cols),int(rows))
plt.imshow(reflected_image_xyaxis)

v)Image Rotation

rows,cols,dim = I.shape
angle = np.radians(15)
RO = np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_image= cv2.warpPerspective(I,RO,(int(cols),int(rows)))
plt.imshow(rotated_image)

vi)Image Cropping
rows,cols,dim = I.shape
cropped_img = I[100:300,100:300]
plt.imshow(cropped_img)

```
## Output:
![output](./l1.png)

### i)Image Translation
![output](./l2.png)

### ii) Image Scaling
![output](./l3.png)

### iii)Image shearing
![output](./l4.png)

### iv)Image Reflection
![output](./l5.png)

### v)Image Rotation
![output](./l6.png)

### vi)Image Cropping
![output](./l7.png)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
