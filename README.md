# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: kolluru pujitha
# Register Number: 212223240074
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
img = cv2.imread('parrot.jpg', cv2.IMREAD_GRAYSCALE)
```

# Display the images.
```
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.show()
```

# Display the images
```
plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Original Image')
plt.show()
```

# Equalize histogram
```
img_eq = cv2.equalizeHist(img)
```

# Display the images.
```
plt.hist(img_eq.ravel(), 256, range = [0, 256])
plt.title('Equalized Histogram')
```

# Display the images.
```
plt.imshow(img_eq, cmap='gray')
plt.title('Original Image')
plt.show()
```

# Read the color image.
```
img = cv2.imread('parrot.jpg', cv2.IMREAD_COLOR)
```

# Convert to HSV.
```
img_hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
```

# Perform histogram equalization only on the V channel, for value intensity.
```
img_hsv[:,:,2] = cv2.equalizeHist(img_hsv[:, :, 2])
```

# Convert back to BGR format.
```
img_eq = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)
```
```
 plt.imshow(img_eq[:,:,::-1]); plt.title('Equalized Image');plt.show()
```
```
plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized');plt.show()
```
# Display the images.
```
#plt.figure(figsize = (20,10))
plt.subplot(221); plt.imshow(img[:, :, ::-1]); plt.title('Original Color Image')
plt.subplot(222); plt.imshow(img_eq[:, :, ::-1]); plt.title('Equalized Image')
plt.subplot(223); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(224); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized');plt.show()
```

# Display the histograms.
```
plt.figure(figsize = [15,4])
plt.subplot(121); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(122); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized')
```

## Output:

<img width="706" height="508" alt="image" src="https://github.com/user-attachments/assets/85305d5f-ee32-4e21-8aee-5ee5d3eed96c" />


<img width="751" height="564" alt="image" src="https://github.com/user-attachments/assets/f3ae83f8-ff8f-4191-bcc4-8e89323e547c" />


<img width="766" height="584" alt="image" src="https://github.com/user-attachments/assets/1c3aa0aa-ff29-42bb-8434-e69e01b80cce" />


<img width="725" height="513" alt="image" src="https://github.com/user-attachments/assets/02968fc1-0102-4c04-b64e-1df3c328f45b" />


<img width="722" height="500" alt="image" src="https://github.com/user-attachments/assets/84de20f7-fbc4-43e5-adc8-3cd1613bf93c" />


<img width="753" height="544" alt="image" src="https://github.com/user-attachments/assets/1fc38657-e77c-4965-8b9b-42c928843558" />


<img width="752" height="533" alt="image" src="https://github.com/user-attachments/assets/12d048d3-59e1-4158-a23e-a57c74558060" />


<img width="838" height="342" alt="image" src="https://github.com/user-attachments/assets/bd1f1ab7-3417-4065-9ad9-d45869459628" />


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
