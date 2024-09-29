# EX-3 Histogram of an images.

### Developed by: Anbuselvan S
### Register No: 212223240008
### Date:

## Aim:
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:
Read the gray and color image using imread().

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step4:
The Histogram of gray scale image and color image is shown.


## Program:   

###  Histogram of Gray scale image and Color image  
```py
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.jpg")
color_image = cv2.imread("color.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
<td>
  
## Output:

### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/b6c4138e-00c9-452a-822b-a7ae98bf8715)

</td>
</tr>



<tr>
  <td width=50%>

### Histogram of Grayscale image and any color image
```py
import numpy as np
import cv2
Gray_image = cv2.imread("gray.jpg")
Color_image = cv2.imread("color.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
</td>
<td>

### Output:

### Histogram of Grayscale image and any color image

#### Grayscale image
![image](https://github.com/user-attachments/assets/78929359-5d5a-4dd3-8cd8-b5d1d1ddc34b)

#### Color image
![image](https://github.com/user-attachments/assets/013ee003-fda3-4e9e-8ab4-85acc3f44477)

</td>
</tr>



<tr>
  <td width=50%>

### Histogram Equalization of Grayscale Image.
```py
import cv2
gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
<td>
  
### Output:

#### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/4d5e1d44-8bbe-478f-98d7-2c7d6e8ea4b3)

</td>
</tr>
</table>

### Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV
