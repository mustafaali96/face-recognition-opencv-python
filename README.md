# face-recognition-opencv-python
power shell:
pip install opencv-contrib-python --upgrade
pip install opencv-python

check if openCV installed: 
C:\> python
import cv2
print(cv2.__version__)
'3.4.0' # your version may be a newer one

create file name camera-test.py:

import numpy as np
import cv2

cap = cv2.VideoCapture(0)

while(True):
    #Capture frame-by-frame
    ret, frame = cap.read()
    #Our operations on the frame come here
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
    #Display the resulting frame
    cv2.imshow('frame',frame)
    cv2.imshow('gray',gray)
    if cv2.waitKey(20) & 0xFF == ord('q'):
        break
    #When everything done, release the capture
cap.release()
cv2.destroyAllWindows()

Now test if camera works:
powershell: python camera-test.py
hit "q" to exit


**********face Recognition**************
create directory
in my case "face_recognition" 
power shell: cd face_recognition

*create virtual env*

mustafa\face_recognition> virtualenv testopencv

if virtualenv not recognize open cmd and run: 
pip install --upgrade virtualenv

move to virtualenv dir: 
mustafa\face_recognition> cd testopencv

now activate it:
mustafa\face_recognition\testopencv> .\Scripts\activate

install dependencies: 
mustafa\face_recognition\testopencv> pip install opencv-contrib-python --upgrade
mustafa\face_recognition\testopencv> pip install image
mustafa\face_recognition\testopencv> pip install Pillow
mustafa\face_recognition\testopencv> python

import cv2
cv2.__version__
exit()

mustafa\face_recognition> git clone "https://github.com/mustafaali96/face-recognition-opencv-python.git"
move src folder to testopencv

powershell:
mustafa\face_recognition\testopencv> cd src
mustafa\face_recognition\testopencv\src> python faces.py
