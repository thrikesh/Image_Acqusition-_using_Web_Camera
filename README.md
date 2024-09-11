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
![Screenshot 2024-03-01 123341](https://github.com/divakar618/Image_Acqusition-_using_Web_Camera/assets/121932143/d25f3d90-9e66-48cd-8d16-ae94f1eac86f)

</br>
</br>

### ii) Display the video
![Screenshot 2024-03-01 123359](https://github.com/divakar618/Image_Acqusition-_using_Web_Camera/assets/121932143/372274ff-0f2a-4f36-8ed2-953d252461a0)

</br>
</br>

### iii) Display the video by resizing the window
![Screenshot 2024-03-01 123415](https://github.com/divakar618/Image_Acqusition-_using_Web_Camera/assets/121932143/0b1665b5-7a90-42a7-89dc-a7b12a31a337)

</br>
</br>

### iv) Rotate and display the video
![Screenshot 2024-03-01 123426](https://github.com/divakar618/Image_Acqusition-_using_Web_Camera/assets/121932143/af88a160-162a-4a26-839f-a790fe8c146d)

</br>
</br>

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
