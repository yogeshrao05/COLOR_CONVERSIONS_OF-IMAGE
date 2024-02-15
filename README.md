# COLOR_CONVERSIONS_OF-IMAGE

## AIM


#### To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv) To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:

### Anaconda - Python 3.7

## Algorithm:


### Step 1

Choose an image and save it as a filename.jpg 

### Step 2

Use imread(filename, flags) to read the file.


### Step 3

Use imshow(window_name, image) to display the image.

### Step 4

Use imwrite(filename, image) to write the image.

### Step 5

End the program and close the output image windows.


### Step 6

Convert BGR and RGB to HSV and GRAY

### Step 7

Convert HSV to RGB and BGR

### Step 8

Convert RGB and BGR to YCrCb

### Step 9

Split and Merge RGB Image


### Step 10

Split and merge HSV Image

 ```python
Developed By: yogesh rao S D
Register Number: 212222110055
```

#### IMAGE 

![dipt 1](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/7080f144-0e18-4774-8c8b-23aa9150cb70)


## Program:


### (i) Read and display the image
 ```py
#Read and display the image
import cv2
image=cv2.imread('city.jpg',1)
image=cv2.resize(image,(200,325))
cv2.imshow('Psv',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output:
![dipt 2](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/c40d254b-3ed6-406b-bfba-a9f4a3c22c58)


## Program:

### (ii) Write the image

```py
#Write the image
import cv2
image=cv2.imread('city.jpg',0)
cv2.imwrite('demos.jpg',image)
```

### Output
![dipt 3](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/7f524adc-5631-4959-80e7-25645960fe8f)


## Program:

### (iii) Shape of the Image

```py
#Shape of the Image
import cv2
image=cv2.imread('city.jpg',1)
print(image.shape)
```


### Output


![dipt 4](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/443f50ec-7bb1-40ba-ba19-3d27b83732dd)


## Program:

### (iv) Access rows and columns
```py
#Access rows and columns
import random
import cv2
image=cv2.imread('city.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output

![dipt 5](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/b01848cf-76ba-4966-8dac-53bcfe8e9467)


## Program:

### (v) Cut and paste portion of image
```py
#Cut and paste portion of image
import cv2
image=cv2.imread('city.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output

![dipt 6](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/d4c4e08c-23cb-4106-9246-7b127f596cee)


### (vi) BGR and RGB to HSV and GRAY
```py
#BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('city.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Original Image
![dipt 7](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/71c2b695-8893-47da-860b-38cfd4c44dee)

### Output
![dipt 8](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/37bfe745-683e-4224-b825-7f1cff29e1f1)



## Program:

### (vii) HSV to RGB and BGR

```py
#HSV to RGB and BGR
import cv2
img = cv2.imread('city.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Original HSV

![dipt 9](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/90abd2df-db8b-4c84-8efc-124304ff95cd)


### Output

![dipt 10](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/028538e3-557b-42c5-95c7-6d2cc6421225)


## Program:

### (viii) RGB and BGR to YCrCb
```py

#RGB and BGR to YCrCb
import cv2
img = cv2.imread('city.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output


![dipt 11](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/cfe5985d-2d31-4b2e-8c62-9baa4cfe4c77)


## Program:

### (ix) Split and merge RGB Image
```py
#Split and merge RGB Image
import cv2
img = cv2.imread('city.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output

#### Channels

![dipt 12](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/9f82c4be-5262-4bf0-8fbf-08d566f2b557)

#### Merged RGB

![dipt 13](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/0bfc7154-13a2-4460-a881-2009f6140abe)



## Program:

### (x) Split and merge HSV Image
```py
#Split and merge HSV Image
import cv2
img = cv2.imread("city.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output

### Merged HSV

![dipt 14](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/373a043a-b402-4c93-891f-db40b3f55b38)



### Splitted

![dipt 15](https://github.com/yogeshrao05/COLOR_CONVERSIONS_OF-IMAGE/assets/122008288/a3e939ef-6558-402f-a113-4cce47539a8e)



## Result:
#### Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
