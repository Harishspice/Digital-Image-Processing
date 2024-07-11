# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.



### Step2:
Load the image file in the program.



### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.



### Step4:
Display the modified image output.



### Step5:
End the program.



## Program:
```python
Developed By: HARISH R
Register Number: 212222110012
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("Photograph.jpg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()


# ii) Image Scaling
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("Photograph.jpg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))

#iii)Image shearing
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("Photograph.jpg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1, 0, 0],
                [0.5, 1, 0],
                [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis
plt.show()

#iv)Image Reflection

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("Photograph.jpg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
# v)Image Rotation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("Photograph.jpg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))
# vi)Image Cropping
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("Photograph.jpg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
cropped_img=input_image[100:300, 100:300]
plt.imshow(cropped_img)


```
## Output:
### i)Image Translation
![image](https://github.com/Harishspice/IMAGE-TRANSFORMATIONS/assets/117935868/a4c7e992-9e12-4f05-af25-3446388ecc07)


### ii) Image Scaling
![image](https://github.com/Harishspice/IMAGE-TRANSFORMATIONS/assets/117935868/1579ff55-1525-4ed9-8a95-3bfcd8c18c0a)



### iii)Image shearing
![image](https://github.com/Harishspice/IMAGE-TRANSFORMATIONS/assets/117935868/9a03ca46-2f35-4675-a6d4-e15422b88a08)



### iv)Image Reflection
![image](https://github.com/Harishspice/IMAGE-TRANSFORMATIONS/assets/117935868/1d2310bb-2606-4b93-9680-5c37cf93174a)



### v)Image Rotation
![image](https://github.com/Harishspice/IMAGE-TRANSFORMATIONS/assets/117935868/de794c6a-5764-4a7e-95c2-a6a4cd3fa31d)



### vi)Image Cropping
![image](https://github.com/Harishspice/IMAGE-TRANSFORMATIONS/assets/117935868/0cb3d85c-08e1-409c-9a8a-24b64cf9b151)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
