### Image Acqusition using Web Camera
### Aim:
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
mport OpenCV Package.

### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
Use cv2.imread to read the video or image

### Step 4:
Use cv2.imshow to show the video

### Step 5:
End the program and close the output video window by pressing 'q'.

## Program: Image_Acqusition-_using_Web_Camera
### Developed By: VEDHASHREE.G
### Register No: 212223240171

## i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)

ret,frame=viedoCaptureObject.read()
cv2.imwrite("m1.jpg",frame)

viedoCaptureObject.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('myimage',frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()
```




## iii) Display the video by resizing the window
```
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read() 
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8) 
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5) 
    image[:height//2, :width//2] = smaller_frame
    image[height//2:, :width//2] = smaller_frame
    image[:height//2, width//2:] = smaller_frame 
    image [height//2:, width//2:] = smaller_frame
    cv2.imshow('myimage', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()


```


## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('RESULT',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image

![Screenshot 2024-09-09 033634](https://github.com/user-attachments/assets/43c1245b-7400-4385-8e55-74a1d2cd4b47)


### ii) Display the video
![Screenshot 2024-09-09 032031](https://github.com/user-attachments/assets/746c5a18-f1bb-4b33-adb6-c7d464e0a423)

![Screenshot 2024-09-09 032315](https://github.com/user-attachments/assets/438df644-54d3-475a-aa06-32022c62a0e7)

### iii) Display the video by resizing the window

![Screenshot 2024-09-09 032234](https://github.com/user-attachments/assets/a7410b9b-c69e-4058-a6d9-d62431a604ea)

### iv) Rotate and display the video
![Screenshot 2024-09-09 032315](https://github.com/user-attachments/assets/8c83a3ff-1676-4e4f-9d0a-d397aa7d5b1b)


## Result:
Thus the image is accessed from webcamera and displayed using openCV.
