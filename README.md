# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.

 
## Program:
~~~
Developed By:U.SRINIVAS
Reg No:212221230108
~~~
``` Python
# Import the necessary packages

import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"U.SRINIVAS",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')

# Use Closing Operation

closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')
```
## Output:

### Display the input Image
<img width="405" alt="image" src="https://github.com/srinivas-aids/Opening-and-Closing/assets/93427183/cbe5020e-baf9-43e8-891b-de9c2553d161">


### Display the result of Opening

<img width="421" alt="image" src="https://github.com/srinivas-aids/Opening-and-Closing/assets/93427183/6743d5c7-8ffd-48bd-a6da-f02f29c7f037">

### Display the result of Closing

<img width="415" alt="image" src="https://github.com/srinivas-aids/Opening-and-Closing/assets/93427183/db753641-df53-45ce-8f0e-026ede0fbf23">

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
