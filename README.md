# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required libraries and read the original image.
<br>

### Step2:
Translate the image.
<br>

### Step3:
Scale the image.
<br>

### Step4:
Shear the image.
<br>

### Step5:
Find reflection of image.
<br>

### Step6:
Rotate the image.

### Step7:
Crop the image.

### Step8:
Display all the Transformed images.

## Program:
```python
Developed By: Manoj Guna Sundar.Tella
Register Number: 212221240026.
i)Image Translation.
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("B2DBy.jpg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M= np.float32([[1, 0, 100],
                [0, 1, 200],
                 [0, 0, 1]])
translated_image =cv2.warpPerspective (input_image, M, (cols, rows))
plt.imshow(translated_image)
plt.show()


ii) Image Scaling.
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("B2DBy.jpg") 
cv2.imshow
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M = np. float32 ([[1.5, 0 ,0],
                 [0, 1.8, 0],
                  [0, 0, 1]])
scaled_img=cv2.warpPerspective(input_image, M, (cols*2, rows*2))
plt.imshow(scaled_img)
plt.show()



iii)Image shearing.
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("B2DBy.jpg") 
cv2.imshow
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x = np.float32([[1, 0.5, 0],
                  [0, 1 ,0],
                  [0, 0, 1]])

M_y = np.float32([[1, 0, 0],
                  [0.5, 1, 0],
                  [0, 0, 1]])
sheared_img_xaxis = cv2.warpPerspective (input_image, M_x, (int(cols *1.5), int (rows *1.5))) 
sheared_img_yaxis = cv2.warpPerspective (input_image, M_y, (int (cols *1.5), int (rows *1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()




iv)Image Reflection.
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("B2DBy.jpg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_yaxis)
plt.show()




v)Image Rotation
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()




vi)Image Cropping
cropped_img=input_image[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()




```
## Output:
### i)Image Translation
![img1](https://user-images.githubusercontent.com/94883876/166099760-1eaf9609-539e-4420-afb6-59a8d9187667.png)

<br>
<br>
<br>
<br>

### ii) Image Scaling
![img2](https://user-images.githubusercontent.com/94883876/166099767-657ba20d-08e9-457f-9305-9ab48bf5b6c5.png)

<br>
<br>
<br>
<br>


### iii)Image shearing
![img3](https://user-images.githubusercontent.com/94883876/166099771-6f7238a9-de0b-4f51-90bf-9ccfd691b65b.png)

<br>
<br>
<br>
<br>


### iv)Image Reflection
![img4](https://user-images.githubusercontent.com/94883876/166099775-b99be455-856e-4f3d-84e4-8bfb281e722a.png)

<br>
<br>
<br>
<br>



### v)Image Rotation
![img5](https://user-images.githubusercontent.com/94883876/166099783-51334c55-7f58-48b9-ac74-3ced9df65cb9.png)

<br>
<br>
<br>
<br>



### vi)Image Cropping
![img6](https://user-images.githubusercontent.com/94883876/166099792-4e915b00-9e6f-41ed-8d6e-33365599f7f3.png)

<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
