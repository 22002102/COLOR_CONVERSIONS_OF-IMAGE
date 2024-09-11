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

### Developed By: 
SANJAY S

### Register Number: 
212222230132

## Program:
```
pip install opencv-python
```
### Read and display the image:
 ```
import cv2
import numpy as np
image_path = 'C:\\Users\\Sanjay\\Downloads\\image.my.jpg'  
image = cv2.imread(image_path)

if image is None:
    print("Error: Image not found!")
else:
    image = cv2.resize(image,(300,500))
    cv2.imshow("image.my.jpg", image)
    cv2.waitKey(0)
```
### Draw Shapes and Add Text
```
cv2.rectangle(image, (20, 20), (50, 50), (125, 0, 0), 2)
cv2.circle(image, (100, 100), 20, (0, 125, 0), 2)
cv2.putText(image, "OpenCV Demo ", (20, 150), cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 0, 125), 2)
cv2.imshow("Image with Shapes and Text", image)
cv2.waitKey(0)
```

### Image Color Conversion.
```
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imshow("Grayscale Image", gray_image)
cv2.waitKey(0)
```

### Access and Manipulate Image Pixels
```
image[100, 100] = [0, 0, 255]
pixel_value = image[100, 100]
print(f"Pixel at (100, 100): {pixel_value}")
cv2.imshow("Modified Pixel Image", image)
cv2.waitKey(0)
```

### Image Resizing (Scale by 50%)
```
resized_image = cv2.resize(image, (0, 0), fx=0.5, fy=0.5)
cv2.imshow("Resized Image", resized_image)
cv2.waitKey(0)
```
### Image Cropping (Crop a region from (50, 50) to (200, 200))
```
cropped_image = image[50:200, 50:200]
cv2.imshow("Cropped Image", cropped_image)
cv2.waitKey(0)
```
### Image Flipping (Flip Horizontally)
```
flipped_image = cv2.flip(image, 1)  # 1 for horizontal flipping
cv2.imshow("Flipped Image", flipped_image)
cv2.waitKey(0)
```
### Write and Save the Modified Image
```
output_path = 'modified_image.jpg'
cv2.imwrite(output_path, image)
print(f"Modified image saved as {output_path}")

cv2.destroyAllWindows()
```

## Output:

### i)Read and Display an Image
![image](https://github.com/user-attachments/assets/8ae74dd5-e058-41e3-bfbc-b5349db43960)


### ii)Draw Shapes and Add Text
![image](https://github.com/user-attachments/assets/5a7e45c1-6df8-43e2-a5b2-36894023c65d)


### iii)Image Color Conversion
![image](https://github.com/user-attachments/assets/7f0419f4-514f-4a95-8439-ca300954fc58)


### iv)Access and Manipulate Image Pixels
![image](https://github.com/user-attachments/assets/369fc775-dd3b-4ec7-8fce-ded2b5411730)

### v)Image Resizing
![image](https://github.com/user-attachments/assets/cdc835b6-d5c4-4e85-b0b5-e356c1f719e7)

### vi)Image Cropping
![image](https://github.com/user-attachments/assets/2873833f-4bc6-4cdf-81ab-40eb96c1fb41)

### vii)Image Flipping
![image](https://github.com/user-attachments/assets/4f65a2f5-08b8-4baa-9a1b-1624dbe27ae3)

### viii)Write and Save the Modified Image
![image](https://github.com/user-attachments/assets/68d304e0-4aa7-4082-9862-98d440f99bb4)
<br>
![image](https://github.com/user-attachments/assets/e3e6b276-2c1d-43c5-be0a-e83be5470b7e)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







