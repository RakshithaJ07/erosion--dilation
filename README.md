# Implementation-of-Erosion-and-Dilation

## Aim:

To implement Erosion and Dilation using Python and OpenCV.

## Software Required:

1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:

Import the necessary pacakages

### Step2:

Create the structuring element

#### Step3:

Create a 5x5 rectangular kernel using cv2.getStructuringElement() for morphological operations.

#### Step4:

Perform erosion and dilation on the image using cv2.erode() and cv2.dilate() with the defined kernel.

#### Step5:

Use matplotlib to display the original, eroded, and dilated images side-by-side for comparison.

 
## Program:

``` Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("sc.jpg")
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
eroded_image = cv2.erode(image, kernel, iterations=1)
dilated_image = cv2.dilate(image, kernel, iterations=1)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(8, 8))
plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
plt.tight_layout()
plt.show()
plt.figure(figsize=(8, 8))
plt.subplot(1, 3, 2)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
plt.tight_layout()
plt.show()
plt.figure(figsize=(8, 8))
plt.subplot(1, 3, 3)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
plt.tight_layout()
plt.show()

```
## Output:

### Display the input Image

![download](https://github.com/user-attachments/assets/ef4603b1-5c73-4b8e-83a3-67f522c196b0)

### Display the Eroded Image

![download](https://github.com/user-attachments/assets/62d49933-a41c-4b32-8ef5-6f47e2340977)

### Display the Dilated Image

![download](https://github.com/user-attachments/assets/28effc1d-dfa1-40e1-b39f-d4acca333172)

## Result
Thus the generated image is eroded and dilated using python and OpenCV.
