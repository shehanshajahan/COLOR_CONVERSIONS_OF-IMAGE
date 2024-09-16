# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By: Shehan Shajahan
### Register Number: 212223240154


## Output:

### i)Read and Display an Image
```
import cv2
image=cv2.imread('Urban.jpg',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('Shehan',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### ii)Draw Shapes and Add Text
1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("Urban.jpg")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (23,123,231), 10)
cv2.imshow('Shehan', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-16 085822](https://github.com/user-attachments/assets/ac2607fe-cc04-48cd-beb9-1f00e201fd74)

2) Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("Urban.jpg")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (21, 55, 122), 10)
cv2.imshow('Shehan', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-16 085838](https://github.com/user-attachments/assets/2adc4e9d-ad52-45b8-adca-ab7cdf39b207)

3.Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("Urban.jpg")
image = cv2.resize(image, (400, 300))
start = (150, 100)
stop = (300, 200)
color = (12, 200, 10)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('Shehan', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-16 085940](https://github.com/user-attachments/assets/1d46fb1c-8971-4738-ad7c-cb5cdadec593)


4. Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("Urban.jpg")
image = cv2.resize(image, (400, 300))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (155, 245, 220) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('Shehan', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-16 090318](https://github.com/user-attachments/assets/2cdd5624-395a-4726-b767-ece1b176b508)


### iii)Image Color Conversion
1. Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('Urban.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('Orginal',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('Converted',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-16 092556](https://github.com/user-attachments/assets/1afd54ae-75c3-4999-92bd-803fbb137117)

2. Convert the image from RGB to GRAY and display it.

```
import cv2
image = cv2.imread('Urban.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('RGB',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('Gray',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-16 092827](https://github.com/user-attachments/assets/aba5f668-3fa1-428a-9459-1d0578ce2b6d)

3. Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('Urban.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('Shehan',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/eb79bd45-d1b2-47d9-986b-c3f94fae8357)

4. 

### iv)Access and Manipulate Image Pixels
<br>
<br>

### v)Image Resizing
<br>
<br>

### vi)Image Cropping
<br>
<br>

### vii)Image Flipping
<br>
<br>

### viii)Write and Save the Modified Image
<br>
<br>






## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







