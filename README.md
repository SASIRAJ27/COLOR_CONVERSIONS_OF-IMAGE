# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step 1: 
Choose an image and save it as a filename.jpg.
### Step 2: 
Use imread(filename, flags) to read the file.
### Step 3: 
Use imshow(window_name, image) to display the image.
### Step 4: 
Use imwrite(filename, image) to write the image.
### Step 5: 
End the program and close the output image windows.
### Step 6: 
Convert BGR and RGB to HSV and GRAY
### Step 7: 
Convert HSV to RGB and BGR
### Step 8: 
Convert RGB and BGR to YCrCb
### Step 9: 
Split and Merge RGB Image
### Step 10: 
Split and merge HSV Image

##### Program:
```
Developed By: SASIRAJKUMAR T J
Register Number:212222230137
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
import cv2
image=cv2.imread('scenery.jpg',1)
image=cv2.resize(image,(400,300))
cv2.imshow('SASIRAJKUMAR',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-16 123303](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/80d9f233-bf84-4fc0-b17a-ebdc9d0efc5b)


  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
import cv2
image=cv2.imread('scenery.jpg',0)
cv2.imwrite('news.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-16 123414](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/edd31dd9-a43a-4ae3-a4ff-cc8e5dfe7604)


  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
import cv2
image=cv2.imread('scenery.jpg',1)
print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-16 123512](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/7c0402ae-d7a0-4ac4-91b4-938a66cba5fe)



  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
import random
import cv2
image=cv2.imread('scenery.jpg',1)
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
  </td>
  <td width="50%">

### OUTPUT:
![Screenshot 2024-02-16 123558](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/2aa1cd83-8064-4add-bbcf-b35257543f51)


  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
 import cv2
 image=cv2.imread('scenery.jpg',1)
 image=cv2.resize(image,(400,400))
 tag =image[150:200,110:160]
 image[110:160,150:200] = tag
 cv2.imshow('partimage1',image)
 cv2.waitKey(0)
 cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![Screenshot 2024-02-16 123633](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/fa578692-687c-41b8-a3cf-714a2fcc7b42)


  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('scenery.jpg',1)
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

### OUTPUT:
![Screenshot 2024-02-16 123746](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/986d865f-7af9-4e9f-ae09-0d88894328a1)


### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('scenery.jpg')
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

### OUTPUT:
![Screenshot 2024-02-16 124515](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/abd9b7b6-655f-41b4-b63b-a1b6564ad881)




### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('scenery.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![Screenshot 2024-02-16 124549](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/29713dab-5c05-4ef4-a7f0-d861e8ee1c8b)



### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('scenery.jpg',1)
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

### OUTPUT:
![Screenshot 2024-02-16 124618](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/b8f78d25-0eed-4d31-b0fa-90fa2bfec6b8)





### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("scenery.jpg",1)
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

### OUTPUT:
![Screenshot 2024-02-16 124648](https://github.com/SASIRAJ27/COLOR_CONVERSIONS_OF-IMAGE/assets/113497176/a159b4d1-136d-42ef-8e6c-5e81110ec862)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.





