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

img=cv2.imread("cat.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
**SOBEL X AXIS :**
```p
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y AXIS :**
```p
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY AXIS :**
```p
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```p
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```p
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR


### SOBEL X AXIS :
![image](https://github.com/Ragu-123/EDGE-DETECTION/assets/113915622/5e9b49cd-01f9-42fa-bd74-9477ee58e540)






### SOBEL Y AXIS :

![image](https://github.com/Ragu-123/EDGE-DETECTION/assets/113915622/243bf74b-f7ae-446f-a607-4456866e1619)




### SOBEL XY AXIS :

![image](https://github.com/Ragu-123/EDGE-DETECTION/assets/113915622/28d02b60-3519-4906-9668-70c4c1c7a316)



### LAPLACIAN EDGE DETECTOR :

![image](https://github.com/Ragu-123/EDGE-DETECTION/assets/113915622/cc498ce9-a9a1-4d0d-a131-2fc0e47a883d)



### CANNY EDGE DETECTOR :

![image](https://github.com/Ragu-123/EDGE-DETECTION/assets/113915622/6d7f7d0e-b4f8-4e40-bd92-d3b886808073)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
