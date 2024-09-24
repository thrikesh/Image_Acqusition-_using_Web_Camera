# Image_Acqusition-_using_Web_Camera
## Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image
<br>

### Step 3:
Use cv2.imwrite to save the image
<br>

### Step 4:
Use cv2.imshow to show the video
<br>

### Step 5:
End the program and close the output video window by pressing 'q'.
<br>

## Program:
``` Python
Developed By: THRIKESH
Register No: 212222230162
```

## i) Write the frame as JPG file
```Python
import cv2
cap = cv2.VideoCapture (0)
frame_number = 0
while frame_number < 5:
    ret, frame = cap.read()
    cv2.imshow('frame', frame)
    cv2.imwrite(f"frame_{frame_number}.jpg", frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```Python
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
```Python
import cv2
cap = cv2.VideoCapture (0) 
cv2.namedWindow('Video', cv2.WINDOW_NORMAL)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    cv2.resizeWindow('Video', 100, 200)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
```Python
import cv2
cap = cv2.VideoCapture (0)
while True:
    ret, frame = cap.read()
    cv2.imshow('Rotated Video', rotated_frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output
### i) Write the frame as JPG image
![image](https://github.com/user-attachments/assets/bfebcec1-8b0b-437f-b0e2-f3df0fc60dd9)


</br>
</br>

### ii) Display the video
![image](https://github.com/user-attachments/assets/dc9bcd9e-10cb-4aee-a8b6-7c5960025f2f)


</br>
</br>

### iii) Display the video by resizing the window
![image](https://github.com/user-attachments/assets/60ca1254-2e15-451b-b00c-37eb1de06399)


</br>
</br>

### iv) Rotate and display the video
![image](https://github.com/user-attachments/assets/c72521ed-08fb-45b6-a8b7-e3f20a331467)

</br>
</br>

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
