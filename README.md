# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import opencv.

### Step2:
Read the original Image.

### Step3:
Store the required conversion of the image in a variable.

### Step4:
Show the image stored in the given variable.

### Step5:
Destroy all the windows and end the program.

## Program:

# Developed By: JAYAKRISHNAN L B L
# Register Number: 212222230052
# i) Convert BGR and RGB to HSV and GRAY

```
import cv2

flower_image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', flower_image)

hsv_bgr_image = cv2.cvtColor(flower_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV', hsv_bgr_image)

hsv_rgb_image = cv2.cvtColor(flower_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV', hsv_rgb_image)

gray_bgr_image = cv2.cvtColor(flower_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', gray_bgr_image)

gray_rgb_image = cv2.cvtColor(flower_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_rgb_image)

cv2.waitKey(0)
cv2.destroyAllWindows()

```

# ii)Convert HSV to RGB and BGR

```
import cv2

flower_hsv_image = cv2.imread('flower.jpg')
cv2.imshow('Original HSV Image', flower_hsv_image)

rgb_image = cv2.cvtColor(flower_hsv_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB', rgb_image)

bgr_image = cv2.cvtColor(flower_hsv_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR', bgr_image)

cv2.waitKey(0)
cv2.destroyAllWindows()



```
# iii)Convert RGB and BGR to YCrCb
```
import cv2
image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', image)
ycrcb_image_rgb = cv2.cvtColor(image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB to YCrCb', ycrcb_image_rgb)
ycrcb_image_bgr = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR to YCrCb', ycrcb_image_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

```



# iv)Split and Merge RGB Image

```
import cv2
image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', image)
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel', blue)
cv2.imshow('G-Channel', green)
cv2.imshow('R-Channel', red)
merged_bgr = cv2.merge((blue, green, red))
cv2.imshow('Merged BGR Image', merged_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

```


# v) Split and merge HSV Image

```
import cv2

image = cv2.imread('flower.jpg')
cv2.imshow('Original Image', image)

hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)

cv2.imshow('Hue - Image', h)
cv2.imshow('Saturation - Image', s)
cv2.imshow('Value - Image', v)

merged_hsv = cv2.merge((h, s, v))
cv2.imshow('Merged HSV Image', merged_hsv)

cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### i) BGR and RGB to HSV and GRAY
   ![Screenshot from 2023-08-23 14-42-28](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/e83e7ebd-61b1-4196-8528-50e6c0e380ad)
   ![Screenshot from 2023-08-23 14-42-47](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/c9760124-cc78-45a5-8867-a11da00af7f1)
   ![Screenshot from 2023-08-23 14-43-33](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/7cda62c0-da7a-4d41-9cfb-f8a57be11448)
   ![Screenshot from 2023-08-23 14-44-24](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/db1b543f-a3e3-4b6a-9948-94eb4f576f03)


### ii) HSV to RGB and BGR
    ![Screenshot from 2023-08-23 14-48-18](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/e9fce7aa-7792-4122-8596-a08e5c2df2d9)
     ![Screenshot from 2023-08-23 14-48-41](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/28f47858-7661-4af5-b044-bd09a49b6904)


### iii) RGB and BGR to YCrCb
    ![Screenshot from 2023-08-23 15-00-19](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/ae86ad5e-188e-4bf2-a445-e932bee7c7c3)
     ![Screenshot from 2023-08-23 15-00-39](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/eda3c988-0137-4a54-b45f-25b48de08d1b)


### iv) Split and merge RGB Image
![Screenshot from 2023-08-23 14-51-06](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/96aa6a95-557e-40d8-9ec2-838a8beecf29)
![Screenshot from 2023-08-23 14-51-27](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/85ce2587-ddee-458f-8602-618956ba0814)
![Screenshot from 2023-08-23 14-51-43](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/81016a03-42f3-4d96-af40-b95ab7ddc252)
![Screenshot from 2023-08-23 14-52-00](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/4d068c5b-9aa6-41a2-af7c-15b1582ee778)


### v) Split and merge HSV Image
![Screenshot from 2023-08-23 14-54-30](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/2ce89581-a9ed-4610-b8c6-b48678ca008c)
![Screenshot from 2023-08-23 14-54-47](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/ee4a1c51-f2de-4c30-ae17-3ef0597d8979)
![Screenshot from 2023-08-23 14-55-06](https://github.com/Jayakrishnan22003251/COLOR-CONVERSION/assets/120232371/08f3e360-8478-433c-bfff-92978f714783)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
