# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)Write and Save the Modified Image


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


## Program:
### i)Read and Display an Image
```
import matplotlib.pyplot as plt
import cv2
img=cv2.imread('img2.jpg')
plt.imshow(img)
plt.show()
```
### ii)Draw Shapes and Add Text
```
res=cv2.line(img,(0,0),(500,500),(205,100,25),10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
```
imc=cv2.imread('img2.jpg')
resc=cv2.circle(imc,(250,250),150,(205,195,185),15)
plt.imshow(resc)
plt.axis('on')
plt.show()
```
```
imr=cv2.imread('img2.jpg')
start=(50,50)
stop=(400,400)
color=(150,150,100)
thick=15
resr=cv2.rectangle(imr,start,stop,color,thick)
plt.imshow(resr)
plt.show()
```
```
imt = cv2.imread("img2.jpg")
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
font_scale = 1
color = (55, 155, 255) 
thickness = 4
rest = cv2.putText(imt, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
plt.imshow(rest)
plt.show()
```
### iii)Image Color Conversion
```
image=cv2.imread("img2.jpg")
imhsv=cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
plt.imshow(imhsv)
plt.show()
```
```
image1=cv2.imread("img2.jpg",0)
imgs=cv2.cvtColor(image1, 0)
plt.imshow(imgs)
plt.show()
```
```
imrgb=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
plt.imshow(imrgb)
plt.show()
```
### iv)Access and Manipulate Image Pixels
```
im2=cv2.imread('img2.jpg')
p=im2[100,100]
p
```
```
imaw=cv2.imread("img2.jpg")
for i in range(100,250):
    for j in range(100,250):
        imaw[i,j]=225
plt.imshow(imaw,cmap="gray")
plt.show()
```
### v)Image Resizing
```
ime=cv2.imread('images.jpg')
ime.shape
```
```
image_resize=cv2.resize(ime,(150,150))
image_resize.shape
```
### vi)Image Cropping
```
imcr=cv2.imread("img2.jpg")
r1=imcr[0:250,0:250]
cv2.imwrite('CR1.jpg',r1)
imgc1=cv2.imread("CR1.jpg")
plt.imshow(imgc1)
plt.show()
```
### vii)Image Flipping
```
imageho = cv2.imread("img2.jpg")
resho=cv2.rotate(imageho,cv2.ROTATE_180)
plt.imshow(resho)
plt.show()
```
```
imageve = cv2.imread("img2.jpg")
resve=cv2.rotate(imageve,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(resve)
plt.show()
```
### viii)Write and Save the Modified Image
```
cv2.imwrite('Saved.jpg',resve)
```


## Developed By: Prajin S
## Register Number: 212223230151


## Output:

### i)Read and Display an Image
![image](https://github.com/user-attachments/assets/3babc8a2-2cfd-41e4-89e3-b1aa50ff68a4)


### ii)Draw Shapes and Add Text
![image](https://github.com/user-attachments/assets/217686d2-dd33-4af7-8200-c9baa839bff4)
![image](https://github.com/user-attachments/assets/8435dcb1-bb7a-4866-9e2e-fffcba12cc44)
![image](https://github.com/user-attachments/assets/ec4c7435-c951-4d67-9319-4ff1f969481a)
![image](https://github.com/user-attachments/assets/3732405c-9b53-4eb8-9c7e-fc74179815fe)




### iii)Image Color Conversion
![image](https://github.com/user-attachments/assets/b478b05c-af85-4960-8f98-2f504ed7cc22)
![image](https://github.com/user-attachments/assets/532e1575-f373-4ae2-896a-69dc9241be23)
![image](https://github.com/user-attachments/assets/5878bd00-23b5-4b53-b36c-17024a099a1a)




### iv)Access and Manipulate Image Pixels
![image](https://github.com/user-attachments/assets/bc9fdafa-32bc-4462-9b14-0ddb5229bd51)
![image](https://github.com/user-attachments/assets/e0467009-8c2e-4ac5-be99-a05fefdb69dc)


### v)Image Resizing
![image](https://github.com/user-attachments/assets/550e09cf-07ef-4a81-88e6-412045582a9e)


### vi)Image Cropping
![image](https://github.com/user-attachments/assets/e391aede-31bc-44de-b0bf-b8352af157ab)


### vii)Image Flipping
![image](https://github.com/user-attachments/assets/266f3993-05cc-4016-b8be-1f389a0f6532)
![image](https://github.com/user-attachments/assets/6d9204e5-36cc-4148-9a2d-7fb8740cc1a7)

### viii)Write and Save the Modified Image
![image](https://github.com/user-attachments/assets/70ce8532-0d39-4ab0-bc45-c82b08a910fc)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
