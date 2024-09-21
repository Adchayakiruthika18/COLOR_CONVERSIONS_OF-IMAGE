## Developed By : ADCHAYA KIRUTHIKA M.S
## Register Number : 212223230005
# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

# Program:

### 1)Read and Display an Image

```Python
import cv2
image=cv2.imread('lokesh.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
 
### OUTPUT:

![image](https://github.com/user-attachments/assets/6be59e60-ce86-45d7-97fb-87a8f7d34a6f)

### 2.) Draw Shapes and Add Text:
i)Draw a line from the top-left to the bottom-right of the image.

```Python

import cv2
img = cv2.imread("lokesh.JPG")
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>
### OUTPUT:

![image](https://github.com/user-attachments/assets/e3a27bac-a61b-4752-b52a-07bf4cda0dac)

### ii)Draw Shapes and Add Text
```Python

import cv2
image = cv2.imread("lokesh.jpg")
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 150, (255,0, 0), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### OUTPUT:

![image](https://github.com/user-attachments/assets/834c5b6c-aef6-4101-8286-aefc8833a112)

### iii)Draw a rectangle around a specific region of interest in the image.
```Python

import cv2
image = cv2.imread("lokesh.JPG")
start=(0,0)
stop=(689,389)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(image,start,stop,color,thickness)
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
 <br>
 <br>

### OUTPUT:

![image](https://github.com/user-attachments/assets/8b560741-f4f2-4556-94d8-03b215646b22)


### iv)Add the text "OpenCV Drawing" at the top-left corner of the image.

 ```Python

import cv2
img = cv2.imread("lokesh.JPG")
text = "OPENCV DRAWING"
position = (50, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>

### OUTPUT:

![image](https://github.com/user-attachments/assets/d22ba7ea-836d-4d0c-a1e0-7737fe1f89c3)

### 3)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```Python

import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### OUTPUT:

![image](https://github.com/user-attachments/assets/0f756ccf-6676-47f4-8efa-09cd8e327f4c)

#### ii.)Convert the image from RGB to GRAY and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output:
![image](https://github.com/user-attachments/assets/94e40033-ac7e-4c26-b212-de969150c960)

#### iii.)Convert the image from RGB to YCrCb and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:
![image](https://github.com/user-attachments/assets/91a532c1-45a8-492f-bd45-1b06811261f4)

#### iv.)Convert the HSV image back to RGB and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/6eeae811-4921-4c60-807b-b20722b980ba)

## 4. Access and Manipulate Image Pixels:
```Python

import cv2
img = cv2.imread('lokesh.jpg', 1)
cv2.imshow('Original Image', img)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
img[199, 199] = [255, 255, 255] 
cv2.imshow('Modified Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:

![image](https://github.com/user-attachments/assets/f7f4945d-e95a-4f30-97c7-8753fcdfa6dc)


![image](https://github.com/user-attachments/assets/94468ffb-9d13-4c06-b638-43b2e7603139)

## 5. Image Resizing:
```Python
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/844b9287-5cb2-46e3-81b9-a0d18057df27)

## 6.Image Cropping:
```Python

import cv2
image1=cv2.imread('lokesh.jpg',1)
x, y = 50, 50
width, height = 100, 100
roi = image1[y:y + height, x:x + width]
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/ebd2f7f8-dda2-4d2f-954c-8512bd153f0c)

## 7.Image Flipping:
i.)Flip the original image horizontally and display it.
```Python

import cv2
img = cv2.imread("lokesh.JPG")
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:

![image](https://github.com/user-attachments/assets/ad30a5d5-5730-4ef7-b360-96307395457e)

#### ii.)Flip the original image vertically and display it.

```Python
import cv2

img = cv2.imread("lokesh.JPG")
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:

![image](https://github.com/user-attachments/assets/082a4875-1de0-42f8-aa4d-103f14b3f531)

## 8. Write and Save the Modified Image:
```Python
import cv2
img = cv2.imread("lokesh.JPG")
cv2.imwrite('lokesh1.jpg',img)
```
<br>
<br>

### Output:

![image](https://github.com/user-attachments/assets/43383114-742c-4e01-b61e-f57d25b373fd)
## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







