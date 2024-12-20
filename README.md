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
circle=cv2.circle(img1, (200,200) ,100, (255, 192, 203), 10)
plt.imshow(circle)
plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/db13a9b4-bf58-4da8-8c40-46f22b971d8a)



iii)Draw a rectangle around a specific region of interest in the image.
```
rectangle=cv2.rectangle(img2,(50,50),(350,350),(255,0,0),10)
plt.imshow(rectangle)
plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/99fc1437-58c9-41a3-bb37-84d87b7f0544)



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
![image](https://github.com/user-attachments/assets/8c8d85e0-dc2e-4e87-b5aa-a0e6d15f078b)


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

<img width="513" alt="Screenshot 2024-09-28 at 3 51 40 PM" src="https://github.com/user-attachments/assets/b2374185-36f9-47b3-91af-34466c094216">




ii.)Convert the image from RGB to GRAY and display it.
```
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
plt.imshow(gray2)
plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/95990f9b-6d4c-4527-9834-9281df56dba4)


iii.)Convert the image from RGB to YCrCb and display it.
```
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
plt.imshow(YCrCb1)
plt.axis('off')
plt.show()

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/4dae25e7-28ef-4416-800e-f2dd651ece89)


iii.)Convert the HSV image back to RGB and display it.
```
BGR = cv2.cvtColor(img3,cv2.COLOR_HSV2BGR)
plt.imshow(BGR)
plt.axis('off')
plt.show()

```
### OUTPUT:
<img width="514" alt="Screenshot 2024-09-28 at 3 55 24 PM" src="https://github.com/user-attachments/assets/116cddbc-1145-4b75-81e9-7888160e3d3e">

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
<img width="515" alt="Screenshot 2024-09-28 at 3 56 17 PM" src="https://github.com/user-attachments/assets/3a5627ca-d308-4750-8ec4-5bcb22839934">


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
![image](https://github.com/user-attachments/assets/1fbed977-8f44-444e-be30-165b1af68f1b)


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
![image](https://github.com/user-attachments/assets/45e6aad1-4883-4f10-aca7-c39c9d5ea21d)

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
![image](https://github.com/user-attachments/assets/5fe25cc9-58b8-4e05-9c33-38a17783a16d)


ii.)Flip the original image vertically and display it.
```
img = cv2.resize(img5,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(res)

plt.axis('off')

```
### OUTPUT:
![image](https://github.com/user-attachments/assets/8b5f9071-b548-4ec2-94b4-44a988d91730)

<br>
<br>

### viii)Write and Save the Modified Image
```
cv2.imwrite('vaathu.jpg',img5)
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/6b624daa-1f40-4ab4-8fe4-eb0237032038)

<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
