# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM

Developed by: HARISH R
Register no: 212222110012

```
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("stonecold.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```


## Output:
![image](https://github.com/Harishspice/EDGE-DETECTION/assets/117935868/b2c64a16-cc5f-4fc4-b250-b5cc506e30c6)

### SOBEL EDGE DETECTOR

![image](https://github.com/Harishspice/EDGE-DETECTION/assets/117935868/a72b68c8-9fd5-45ad-8b3e-5a58f750bdf9)
![image](https://github.com/Harishspice/EDGE-DETECTION/assets/117935868/eedae284-d014-41ac-b0f8-aec863880977)
![image](https://github.com/Harishspice/EDGE-DETECTION/assets/117935868/5e692da5-423b-47bc-879d-40cf4b7a6cc9)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Harishspice/EDGE-DETECTION/assets/117935868/87374a40-de7c-4fb8-b761-d6a6f3851e6e)



### CANNY EDGE DETECTOR
![image](https://github.com/Harishspice/EDGE-DETECTION/assets/117935868/a1bc94f0-7b50-44b2-9a6e-b6eb9f027d19)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
