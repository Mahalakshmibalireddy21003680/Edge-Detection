# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:
Import all the required packages.

### Step2:
Load the image to operate on.

### Step3:
Convert the image to grayscale image.

### Step4:
Use Sobel operator along x,y and xy directions.

### Step5:
Operate the image using Laplacian operator.

### Step6:
Operate the image using Canny Edge operator.

### Step7:
Show all the operated images output.

 
## Program:

``` Python

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("car.png")
cv2.imshow("Original Image",image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

## SOBEL EDGE DETETCTOR:
### SOBEL X:

sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL Y:

sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL XY:

sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()


## LAPLACIAN EDGE DETECTOR:

laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()


## CANNY EDGE DETECTOR:

canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR

#### SOBEL X
<img width="594" alt="1" src="https://user-images.githubusercontent.com/93427286/170657103-9f2695af-3674-4f0d-87b1-36927a52ae07.png">


#### SOBEL Y
<img width="594" alt="2" src="https://user-images.githubusercontent.com/93427286/170657176-0c66b83a-b68b-4a47-a5fc-05792ad65f7d.png">


#### SOBEL XY
<img width="594" alt="3" src="https://user-images.githubusercontent.com/93427286/170657263-9bdb3364-a401-4bb7-a02e-9c5ed0a784ef.png">



### LAPLACIAN EDGE DETECTOR

<img width="594" alt="4" src="https://user-images.githubusercontent.com/93427286/170657316-d1471b17-5742-4635-8740-4716aa51874d.png">



### CANNY EDGE DETECTOR

<img width="594" alt="5" src="https://user-images.githubusercontent.com/93427286/170657372-5140634f-0b37-4e26-a5ca-6e09c6ddf1d2.png">


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
