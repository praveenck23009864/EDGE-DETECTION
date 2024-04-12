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

## PROGRAM :
### DEVELOPED BY : THANJIYAPPAN K
### REGISTER NO : 212222240108
### Convert image to grayscale and remove noise
```P
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("duck.png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray1 = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
**SOBEL X AXIS :**
```p
sobelx = cv2.Sobel(gray1,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray1,cmap='gray')
plt.title("Gray Image")
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.xticks([])
plt.yticks([])
plt.show()
```
**SOBEL Y AXIS :**
```p
sobely = cv2.Sobel(gray1,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray1,cmap='gray')
plt.title("Original Image")
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.xticks([])
plt.yticks([])
plt.show()
```
**SOBEL XY AXIS :**
```p
sobelxy = cv2.Sobel(gray1,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray1,cmap='gray')
plt.title("Gray Image")
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.xticks([])
plt.yticks([])
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```p
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray1,cmap='gray')
plt.title("Gray Image")
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='gray')
plt.title("laplacian")
plt.xticks([])
plt.yticks([])
plt.show()
```
### CANNY EDGE DETECTOR
```p
canny_edges = cv2.Canny(img, 120, 150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray1,cmap='gray')
plt.title("Gray Image")
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR


### SOBEL X AXIS :
![image](https://github.com/22009011/EDGE-DETECTION/assets/118343461/b798cd40-fc9a-40f6-ae3c-84e3079e5a9b)







### SOBEL Y AXIS :

![image](https://github.com/22009011/EDGE-DETECTION/assets/118343461/2b91a1f5-739f-42ff-a2b1-453356dc183a)





### SOBEL XY AXIS :

![image](https://github.com/22009011/EDGE-DETECTION/assets/118343461/63a9f2e9-adc9-426d-b6c5-8de40b0ec864)




### LAPLACIAN EDGE DETECTOR :
![image](https://github.com/22009011/EDGE-DETECTION/assets/118343461/a3428e4b-9aa4-4a5f-a1d1-d600428c3632)




### CANNY EDGE DETECTOR :

![image](https://github.com/22009011/EDGE-DETECTION/assets/118343461/8b539e47-6887-4584-9601-2e56b51d96a6)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
