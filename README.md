# COLOR_CONVERSIONS_OF-IMAGE.

### Developed by: Chandrasekar S
### Register No: 212222230025
### Date:

## AIM:
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

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
      o Load an image from your local directory and display it.

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

### Developed By: Chandrasekar S
### Register Number: 212222230025

```
import cv2

image = cv2.imread('sample2.JPG') 
cv2.imshow('Original Image', image)
cv2.waitKey(0)

cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255, 0, 0), 5)

center_x, center_y = image.shape[1] // 2, image.shape[0] // 2

cv2.circle(image, (center_x, center_y), 50, (0, 255, 0), 5)

cv2.rectangle(image, (50, 50), (150, 150), (0, 0, 255), 5)

cv2.putText(image, 'OpenCV Drawing', (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 2)

cv2.imshow('Image with Drawing', image)
cv2.waitKey(0)

hsv_image = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
cv2.imshow('HSV Image', hsv_image)
cv2.waitKey(0)

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imshow('Gray Image', gray_image)
cv2.waitKey(0)

ycrcb_image = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('YCrCb Image', ycrcb_image)
cv2.waitKey(0)

rgb_from_hsv = cv2.cvtColor(hsv_image, cv2.COLOR_HSV2BGR)
cv2.imshow('RGB from HSV', rgb_from_hsv)
cv2.waitKey(0)

pixel_value = image[100, 100]
print(f'Pixel value at (100, 100): {pixel_value}')

image[200, 200] = [255, 255, 255]

resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('Resized Image (Half Size)', resized_image)
cv2.waitKey(0)

roi = image[50:150, 50:150]  
cv2.imshow('Cropped ROI', roi)
cv2.waitKey(0)

flipped_horizontally = cv2.flip(image, 1)
flipped_vertically = cv2.flip(image, 0)

cv2.imshow('Flipped Horizontally', flipped_horizontally)
cv2.waitKey(0)

cv2.imshow('Flipped Vertically', flipped_vertically)
cv2.waitKey(0)

cv2.imwrite('modified_image.jpg', image)

cv2.destroyAllWindows()
```

## Output:

### i)Read and Display an Image:
![image](https://github.com/user-attachments/assets/bf020b86-e626-43f1-a485-ff5086dbf828)


### ii)Draw Shapes and Add Text:
![image](https://github.com/user-attachments/assets/f61c1060-1ec4-48ca-932e-95a7ea28850c)


### iii)Image Color Conversion:

#### HSV image:
![Screenshot 2024-09-16 083613](https://github.com/user-attachments/assets/49596ead-4c5e-4f64-b8de-46b013eb7048)

#### Gray image:
![Screenshot 2024-09-16 083643](https://github.com/user-attachments/assets/99f5ea37-9ec8-4fd8-85b5-a3645d9ae6cc)

#### YCrCb image:
![Screenshot 2024-09-16 083709](https://github.com/user-attachments/assets/6b747454-3d46-4f53-8ace-5b4649440fee)

#### RGB from HSV:
![Screenshot 2024-09-16 083740](https://github.com/user-attachments/assets/044d94d5-68c1-401b-8838-e3e8eb21c180)

### iv)Access and Manipulate Image Pixels:
![Screenshot 2024-09-16 083806](https://github.com/user-attachments/assets/76864aa7-fb04-4e23-adcd-a301b2cfa1a0)

### v)Image Resizing:
![Screenshot 2024-09-16 083844](https://github.com/user-attachments/assets/d2b77411-8698-4f5a-b902-d5d6de66f36e)

### vi)Image Cropping:
![Screenshot 2024-09-16 083917](https://github.com/user-attachments/assets/bc02a723-0706-4773-b578-1113a662dd5f)

### vii)Image Flipping:

#### Horizontal:
![Screenshot 2024-09-16 083956](https://github.com/user-attachments/assets/81cfaaa2-5185-4fea-a714-da79c0bd870d)

#### Vertical:
![Screenshot 2024-09-16 084025](https://github.com/user-attachments/assets/bd25bf76-ede9-4ebe-b38d-693b7d169388)

### viii)Write and Save the Modified Image:
![Screenshot 2024-09-16 084957](https://github.com/user-attachments/assets/2f525971-40ad-4e88-a25e-51350e9840a7)
![Screenshot 2024-09-16 085018](https://github.com/user-attachments/assets/9d65935d-090d-41e4-8218-814d6ae7a683)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







