# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.
<br>
### Step2:
Read the image and convert the bgr image to gray scale image.
<br>
### Step3:
Use any filters for smoothing the image to reduse the noise.
<br>
### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
<br>
### Step5:
Display the filtered image using plot and imshow.
<br>

## Program:

```
DEVELOPED BY: Yamunaasri T S
REG NO : 212222240117
```
# Import the packages
```
import cv2
import matplotlib.pyplot as pl
```
# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("gojo.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR
## SOBEL X
```
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
## SOBEL Y
```
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
## SOBEL XY
```
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
# LAPLACIAN EDGE DETECTOR
```
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

# CANNY EDGE DETECTOR
```
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
#### SOBEL X
![Screenshot 2023-10-11 161814](https://github.com/Yamunaasri/EDGEDETECTION/assets/115707860/e3af0473-36e5-4210-bd65-abe971d19671)

#### SOBEL Y
![Screenshot 2023-10-11 161945](https://github.com/Yamunaasri/EDGEDETECTION/assets/115707860/500d4c4c-5f93-4e7d-ac81-40c4efcc01d1)

#### SOBEL XY
![Screenshot 2023-10-11 162120](https://github.com/Yamunaasri/EDGEDETECTION/assets/115707860/7ec6da2d-9287-457f-b9a1-7d747cc28b33)

### LAPLACIAN EDGE DETECTOR
![Screenshot 2023-10-11 162146](https://github.com/Yamunaasri/EDGEDETECTION/assets/115707860/795fb662-f728-43a8-bad2-2a00fb27ca06)

### CANNY EDGE DETECTOR
![Screenshot 2023-10-11 162217](https://github.com/Yamunaasri/EDGEDETECTION/assets/115707860/dd97f663-2534-4fe2-a6a7-ad60ddefce37)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
