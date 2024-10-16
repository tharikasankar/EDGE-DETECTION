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
## PROGRAM:
```
DEVELOPED BY: Tharika S
REGISTER NUMBER: 212222230159
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("lotus.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![image](https://github.com/user-attachments/assets/5a5d2927-3d4b-4a59-a609-f69785e00f65)

### SOBEL EDGE DETECTOR
![image](https://github.com/user-attachments/assets/ad3ee93f-c50c-44e1-b60a-78fddde5ab38)

![image](https://github.com/user-attachments/assets/815e6572-b8bf-4011-95e6-712c73e99878)

![image](https://github.com/user-attachments/assets/344f94e5-3ab5-48ba-b31e-f21a79397a68)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/user-attachments/assets/7dc57f3a-7d99-45ec-baf3-45660f7d680b)



### CANNY EDGE DETECTOR
![image](https://github.com/user-attachments/assets/2b90a9ad-ecc4-4cb4-b793-96b7a95cfb11)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
