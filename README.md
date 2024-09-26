# Image Acqusition using Web Camera
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
cap = cv2.VideoCapture(0)
frame_number = 0
 # Initialize frame number
while frame_number < 5:
ret, frame = cap.read()
cv2.imshow('frame', frame)
# Save frame as JPG file
cv2.imwrite(f"frame_{frame_number}.jpg", frame)
frame_number += 1
if cv2.waitKey(1) & 0xFF == ord('q'):
break
cap.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```
import cv2 
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

## iii) Display the video by resizing the window
```
import cv2
cap = cv2.VideoCapture(0)
# Create a resizable window
cv2.namedWindow('Video', cv2.WINDOW_NORMAL)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    # Resize the window
    cv2.resizeWindow('Video', 50, 200)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
```
import cv2
cap = cv2.VideoCapture (0) # Define the rotation angle (in degrees) rotation_angle = 90
while True:
    ret, frame = cap.read()
# Rotate the frame 
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)

    cv2.imshow('Rotated Video', rotated_frame)

    if cv2.waitKey(1) & 0xFF == ord('q'):

        break

cap.release()

cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image

![WhatsApp Image 2024-09-26 at 15 52 35_29d711a5](https://github.com/user-attachments/assets/947bbbdf-b8b6-4f15-9f86-2b6fd8b67979)



### ii) Display the video


![WhatsApp Image 2024-09-26 at 15 48 24_f1ed9dc2](https://github.com/user-attachments/assets/1a705710-44e0-4a95-b4d7-b102bd3a067c)





### iii) Display the video by resizing the window



![WhatsApp Image 2024-09-26 at 15 46 52_d9bcfa39](https://github.com/user-attachments/assets/20c82255-0aad-4a3b-bb03-0f53cda4342d)



### iv) Rotate and display the video
![WhatsApp Image 2024-09-26 at 15 35 23_26967107](https://github.com/user-attachments/assets/8b77db63-d4c2-4806-b691-0954ae360bbd)


## Result:
Thus the image is accessed from webcamera and displayed using openCV.
