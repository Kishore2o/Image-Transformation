# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Find reflection of image.

### step6:
Rotate the image.

### Step7:
Crop the image.

### Step8:
Display all the Transformed images.

## Program:
```python
Developed By:S.Kishore
Register Number:212222240050
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("lion.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape

i)Image Translation

M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

ii) Image Scaling
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()


iii)Image shearing
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()


iv)Image Reflection
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()



v)Image Rotation
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()



vi)Image Cropping

cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()




```
## Output:
### Input Image
![1st (1)](https://user-images.githubusercontent.com/118679883/232666901-b466401a-9eec-4094-a662-51bf5ef5cb8d.png)


### i)Image Translation
![2nd (2)](https://user-images.githubusercontent.com/118679883/232667968-52a5432f-e334-4c8e-a87e-454c6f10fcf3.png)


### ii) Image Scaling
![3rd (2)](https://user-images.githubusercontent.com/118679883/232667917-4ae0c1b1-85bb-474b-a439-bcb79cb13c69.png)



### iii)Image shearing
![4th (2)](https://user-images.githubusercontent.com/118679883/232667881-1ee19301-b382-421f-acf6-823821d9f0d7.png)

![5th (1)](https://user-images.githubusercontent.com/118679883/232667854-599c3536-57e5-4f1e-8f1b-2439fd9aec19.png)



### iv)Image Reflection
![6th (1)](https://user-images.githubusercontent.com/118679883/232667823-bf7c8a7d-bb9b-4284-a2a7-fec56f7d7fc5.png)

![7th (1)](https://user-images.githubusercontent.com/118679883/232667795-d1a7833d-a264-4be2-a207-78617af4a29e.png)




### v)Image Rotation
![8th (1)](https://user-images.githubusercontent.com/118679883/232667762-d367435d-7619-4161-9af2-7f00c75d5e13.png)




### vi)Image Cropping
![9th (2)](https://user-images.githubusercontent.com/118679883/232667689-e116d008-b94a-462b-977b-88f0c8647fac.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
