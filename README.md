Develop the program to perform linear transformation on a image.


import cv2
 
img = cv2.imread('k.jpg')
(h, w) = img.shape[:2]
center = (w / 2, h / 2)

 
angle90 = 90
angle180 = 180
angle270 = 270
 
scale = 1.0
 
M = cv2.getRotationMatrix2D(center, angle90, scale)
rotated90 = cv2.warpAffine(img, M, (h, w))

M = cv2.getRotationMatrix2D(center, angle180, scale)
rotated180 = cv2.warpAffine(img, M, (w, h))
 
M = cv2.getRotationMatrix2D(center, angle270, scale)
rotated270 = cv2.warpAffine(img, M, (h, w))
 
 
cv2.imshow('Original Image',img)
cv2.waitKey(0) 
cv2.destroyAllWindows()
 
cv2.imshow('90 degree',rotated90)
cv2.waitKey(0) 
cv2.destroyAllWindows() 
 
cv2.imshow('180 degree',rotated180)
cv2.waitKey(0) 
cv2.destroyAllWindows() 
 
cv2.imshow('270 degree',rotated270)
cv2.waitKey(0)
cv2.destroyAllWindows()



![image](https://user-images.githubusercontent.com/96233848/148202384-ae507926-fe80-4ba5-ba5e-c005af2ba8ed.png)
![image](https://user-images.githubusercontent.com/96233848/148202509-6bd3c009-ed3a-49bd-bec3-df4726618c5d.png)
![image](https://user-images.githubusercontent.com/96233848/148202603-297da684-e76d-44ac-897b-72410e72e8c9.png)
![image](https://user-images.githubusercontent.com/96233848/148202671-ed3ca232-7a15-4cef-9cda-1565a5a12dad.png)














