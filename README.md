## Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
### Program:
```
Name  : Sathish R
reg No: 212222230138
```

##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'SATHISH',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:

#### Display the input Image
![dip_ex-9-1](https://github.com/r-sathish-02/erosion--dilation/assets/118787261/5fc8b015-f7a4-4ecc-a1e7-fc9c140fb46c)


#### Display the Eroded Image
![dip-exp-9-2](https://github.com/r-sathish-02/erosion--dilation/assets/118787261/89bfdd90-d990-4132-bbf6-33590f473e2d)



#### Display the Dilated Image
![dip-ex-9-3](https://github.com/r-sathish-02/erosion--dilation/assets/118787261/d773853c-4508-436b-94f1-0d0b99d62ed6)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
