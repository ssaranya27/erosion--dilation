## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step-1:
Create a black image of size 100x600 pixels.

## Step-2:
Use a specified font to write the word "Lifestyle" on the image at a defined position.

## Step-3:
Show the image containing the text without axis labels.

## Step-4:
Define a structuring element for morphological operations (e.g., a cross-shaped kernel).

## Step-5:
Apply erosion to the image using the defined structuring element to reduce the size of white regions.

## Step-6:
Apply dilation to the original image using the same structuring element to increase the size of white regions.

 
## Program:
### DEVELOPED BY : SARANYA S
### REG NO : 212223220101

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100, 600, 3), dtype='uint8')  # Black background (RGB: 0, 0, 0)
font = cv2.FONT_HERSHEY_COMPLEX
text_color = (255, 255, 255)  # White text (RGB: 255, 255, 255)
cv2.putText(img, 'Ayisha Rinsi K', (60, 70), font, 2, text_color, 5, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```


# Create the structuring element

```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```

# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



# Dilate the image

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
## Output:

### Display the input Image
<br>
<br>
<img width="482" height="75" alt="image" src="https://github.com/user-attachments/assets/57348416-2e95-4c41-adcf-55c595869698" />


<br>
<br>
<br>

### Display the structured elements
<br>
<br>
<img width="236" height="532" alt="image" src="https://github.com/user-attachments/assets/95605bff-37cf-433a-97cc-c7b98cb0467d" />


<br>
<br>
<br>


### Display the Eroded Image
<br>
<br>
<img width="437" height="67" alt="image" src="https://github.com/user-attachments/assets/76c7f404-4416-4680-91ad-e97f09d02c62" />



<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<img width="437" height="69" alt="image" src="https://github.com/user-attachments/assets/7995b3ce-6311-4fcf-93cb-816bdbc7bda6" />




<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
