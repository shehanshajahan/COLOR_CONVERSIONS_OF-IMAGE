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
import matplotlib.pyplot as plt
import cv2
img=cv2.imread('beauty.jpg')
plt.imshow(img)
plt.show()
```
![image](https://github.com/user-attachments/assets/dfdc0b41-efd0-45f7-a202-1e3fc04c47ac)


### ii)Draw Shapes and Add Text
1) Draw a line from the top-left to the bottom-right of the image.
```
res=cv2.line(img,(0,0),(600,400),(205,100,250),10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/c2dbced5-3cc4-4f2c-87d5-26c30c4cc785)



2) Draw a circle at the center of the image.
```
imc=cv2.imread('beauty.jpg')
resc=cv2.circle(imc,(250,250),100,(250,195,280),15)
plt.imshow(resc)
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/7fe7ab28-d8e5-4488-96fc-850a8f8ce487)



3.Draw a rectangle around a specific region of interest in the image.
```
imr=cv2.imread('beauty.jpg')
start=(50,50)
stop=(300,300)
color=(250,250,200)
thick=15
resr=cv2.rectangle(imr,start,stop,color,thick)
plt.imshow(resr)
plt.show()
```
![image](https://github.com/user-attachments/assets/a934f228-14ce-4644-a6c6-04d4124d3070)



4. Add the text "OpenCV Drawing" at the top-left corner of the image.
```
imt = cv2.imread("beauty.jpg")
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
font_scale = 1
color = (150, 155, 255) 
thickness = 3
rest = cv2.putText(imt, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
plt.imshow(rest)
plt.show()

```
![image](https://github.com/user-attachments/assets/0c461c01-9afb-42f0-803d-826e707e53cb)




### iii)Image Color Conversion
1. Convert the image from RGB to HSV and display it
```
image=cv2.imread("beauty.jpg")
imhsv=cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
plt.imshow(imhsv)
plt.show()
```
![image](https://github.com/user-attachments/assets/adec2407-9e58-4574-bc18-18ea19e9fcd7)


2. Convert the image from RGB to GRAY and display it.

```
image1=cv2.imread("beauty.jpg",0)
imgs=cv2.cvtColor(image1, 0)
plt.imshow(imgs)
plt.show()
```
![image](https://github.com/user-attachments/assets/64d186cd-0115-4dd1-ba3e-04b199ffe3cc)



3. Convert the image from RGB to YCrCb and display it.
```
imrgb=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
plt.imshow(imrgb)
plt.show()
```
![image](https://github.com/user-attachments/assets/38083ba7-9c6a-429c-86c3-58471d807174)


### iv)Access and Manipulate Image Pixels
1. Access and print the value of the pixel at coordinates (100, 100)
```
im2=cv2.imread('beauty.jpg')
p=im2[100,100]
p
```
![image](https://github.com/user-attachments/assets/e57c28a8-b1f6-4d78-98f5-e3278fb53764)



2. Modify the color of the pixel at (200, 200) to white.
```
imaw=cv2.imread("beauty.jpg")
for i in range(100,250):
    for j in range(100,250):
        imaw[i,j]=225
plt.imshow(imaw,cmap="gray")
plt.show()
```
![image](https://github.com/user-attachments/assets/9fcbb7f3-8437-4879-a2eb-a5cc33aefbed)



### v)Image Resizing
Resize the original image to half its size and display it.
```
ime=cv2.imread('beauty.jpg')
ime.shape
```
![image](https://github.com/user-attachments/assets/ecb61238-611c-4b06-9bae-f78dfdf052c5)
```
image_resize=cv2.resize(ime,(150,150))
image_resize.shape
```
![image](https://github.com/user-attachments/assets/424c628b-5be5-445c-b528-acb19eda96c2)



### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
imcr=cv2.imread("beauty.jpg")
r1=imcr[0:250,0:250]
cv2.imwrite('CR1.jpg',r1)
imgc1=cv2.imread("CR1.jpg")
plt.imshow(imgc1)
plt.show()
```
![image](https://github.com/user-attachments/assets/0d012913-c841-43a6-9eef-4a687fb395eb)




### vii)Image Flipping
1. Flip the original image horizontally and display it.
```
imageho = cv2.imread("beauty.jpg")
resho=cv2.rotate(imageho,cv2.ROTATE_180)
plt.imshow(resho)
plt.show()
```
![image](https://github.com/user-attachments/assets/a02499f3-8f0d-4d49-a44d-7d3a9704c529)



2. Flip the original image vertically and display it.
```
imageve = cv2.imread("beauty.jpg")
resve=cv2.rotate(imageve,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(resve)
plt.show()
```
![image](https://github.com/user-attachments/assets/e2b4e179-7011-4500-aa5b-9a59328c4ad2)



### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
cv2.imwrite('Saved.jpg',resve)
```
![image](https://github.com/user-attachments/assets/11ba08ea-1e42-4312-bd70-3ab32130e989)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
