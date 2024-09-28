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
### Developed By: Chandrasekar S
### Register Number: 212222230025

## Output:


### i)Read and Display an Image
```
import cv2
import matplotlib.pyplot as plt
img=cv2.imread('birds.jpg')
plt.imshow(img)
plt.axis('off')
plt.show()

```
### OUTPUT:
<img width="513" alt="Screenshot 2024-09-28 at 3 27 49 PM" src="https://github.com/user-attachments/assets/74bdf061-979a-41d7-9619-3dbc9a966805">


<br>
<br>

 *Note:Changing the shape as the original image is too large.*

### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image.
```
res = cv2.line(img2, (0, 0), (400, 400), (255, 0, 0), 3)
plt.imshow(res)
plt.axis('off')
plt.show()

```
### OUTPUT:
<img width="386" alt="Screenshot 2024-09-28 at 3 30 05 PM" src="https://github.com/user-attachments/assets/28f65c6f-bdd7-4e4d-9e9c-2101d52a2328">


ii)Draw a circle at the center of the image.
```
circle=cv2.circle(img1, (200,200) ,100, (0, 0, 255), 10)
plt.imshow(circle)
plt.axis('off')
plt.show()

```
### OUTPUT:
<img width="384" alt="Screenshot 2024-09-28 at 3 31 36 PM" src="https://github.com/user-attachments/assets/3dbaa6ba-4f1b-48f4-95d1-116991497125">


iii)Draw a rectangle around a specific region of interest in the image.
```
rectangle=cv2.rectangle(img2,(50,50),(350,350),(255,255,0),10)
plt.imshow(rectangle)
plt.axis('off')
plt.show()

```
### OUTPUT:
<img width="391" alt="Screenshot 2024-09-28 at 3 32 21 PM" src="https://github.com/user-attachments/assets/bb6658f8-0804-4c31-ba76-07cf688541b5">


iv)Add the text at the bottom of the image.
```
img3=cv2.imread('birds.jpg')
img4=cv2.resize(img,(400,400))

text = "You want a smooch?"
position = (140, 300)
font=cv2.FONT_HERSHEY_SIMPLEX

res = cv2.putText(img4, text , (40,280) , font , 1 , (255,255,255) , 5 , cv2.LINE_AA)
plt.imshow(img4)
plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/7b7fa703-d7fe-459b-a27e-938560255e2b)


<br>
<br>

### iii)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```
cv2.imshow('Original Image',img3)
hsv2 = cv2.cvtColor(img3,cv2.COLOR_RGB2HSV)
plt.imshow(img3)
plt.imshow(hsv2)
plt.axis('off')
plt.show()

```
### OUTPUT:

![image](https://github.com/user-attachments/assets/20f0c8b6-bd65-442a-923d-74822cb2c16b)




ii.)Convert the image from RGB to GRAY and display it.
```
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
plt.imshow(gray2)
plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/c8b0802d-c293-44b6-8714-273ed4c4daad)


iii.)Convert the image from RGB to YCrCb and display it.
```
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
plt.imshow(YCrCb1)
plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/7a256ed0-f81c-49a1-b4d9-6ee6995da2dc)


iii.)Convert the HSV image back to RGB and display it.
```
BGR = cv2.cvtColor(img3,cv2.COLOR_HSV2BGR)
plt.imshow(BGR)
plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/f13144d5-5452-4874-a26b-8adb17b4aeba)

<br>
<br>

### iv)Access and Manipulate Image Pixels
```
pixel_value = img3[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
img3[199, 199] = [255, 255, 255]
plt.imshow(img3)
plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/31ac5dac-ab8c-446e-9909-1f499237b579)


<br>
<br>

### v)Image Resizing
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(img, (300, 400))
plt.imshow(resized_img)

plt.axis('off')
plt.show()

```
### OUTPUT:

<br>
<br>

### vi)Image Cropping
```


x, y = 50, 50
width, height = 150, 150
roi = img[y:y + height, x:x + width]
plt.imshow(roi)

plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/0cfed28a-8901-40fc-9770-d4b1f082eb0a)

<br>
<br>

### vii)Image Flipping
i.)Flip the original image horizontally and display it.
```
img5=cv2.imread('birds.jpg')
res=cv2.rotate(img5,cv2.ROTATE_180)

plt.imshow(res)

plt.axis('off')

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/a324ca07-c93a-4fcb-964b-6139e84bd858)


ii.)Flip the original image vertically and display it.
```
img = cv2.resize(img5,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(res)

plt.axis('off')

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/3de773ae-8cb0-40bb-9dd6-e8472b089b99)

<br>
<br>

### viii)Write and Save the Modified Image
```
cv2.imwrite('vaathu.jpg',img5)
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/3ad0b07f-16e5-4ff1-9f74-9402285ac760)

<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
