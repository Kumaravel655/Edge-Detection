# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.
<br>


### Step2:
For performing edge detection on a image.

* Sobel
```
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)
```

* Laplacian
```
Laplacian=cv2.Laplacian(img,cv2.CV_64F)
```

* Canny
```
canny=cv2.Canny(img,120,150)
```
<br>

### Step3:
Display all the images with their respective edge detected images.
<br>


 
## Program:

``` Python
# Import the packages
import cv2 
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("leaf.jpg",0)
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
img=cv2.GaussianBlur(img,(3,3),0)
plt.imshow(img)
plt.axis("off")
plt.show()

# SOBEL EDGE DETECTOR
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)

# LAPLACIAN EDGE DETECTOR
Laplacian=cv2.Laplacian(img,cv2.CV_64F)

# CANNY EDGE DETECTOR
canny=cv2.Canny(img,120,150)

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel X axis')
plt.imshow(sobelx)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel Y axis')
plt.imshow(sobely)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel X and Y axis')
plt.imshow(sobelxy)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian')
plt.imshow(Laplacian)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Canny')
plt.imshow(canny)
plt.show()


```

## Output:
### SOBEL EDGE DETECTOR
![Screenshot (110)](https://user-images.githubusercontent.com/75235334/168867245-833933e6-929c-437e-af94-e58b4d273730.png)
![Screenshot (111)](https://user-images.githubusercontent.com/75235334/168867750-1f9ce98f-83d9-45f4-9a5d-cbf1fcafcaa3.png)
![Screenshot (112)](https://user-images.githubusercontent.com/75235334/168868122-db266485-8fa0-41fb-ad73-5f3d6aa88ca4.png)
<br>
<br>
<br>
<br>
<br>
<br>


### LAPLACIAN EDGE DETECTOR
![Screenshot (114)](https://user-images.githubusercontent.com/75235334/168868716-0c71158d-6be6-4ce9-958f-f0de78083f1a.png)
<br>
<br>
<br>
<br>
<br>
<br>


### CANNY EDGE DETECTOR
![Screenshot_639](https://user-images.githubusercontent.com/75235455/168431082-29f746c4-80e8-484e-b3a2-1a9c666754b8.png)
<br>
<br>
<br>
<br>
<br>
<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
