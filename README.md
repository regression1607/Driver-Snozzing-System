# Driver-Snozzing-System
A Driver snoozing system, is a technology designed to detect when a driver is experiencing drowsiness or fatigue while driving. This can be a serious safety concern, as drowsy driving can lead to accidents on the road.


The algorithm for the above code is as follows:

1.First, the code imports the necessary libraries, including cv2, numpy, dlib, and pygame. It also initializes pygame and loads a sound file to be played later.

2.The code then sets up a face detector and a predictor using dlib.

3.The code defines some variables to keep track of the user's sleep, drowsy, and active states. It also defines a variable to store the current status and a color tuple to be used for displaying text on the frame.

4.The code defines a function called compute which takes two points as input and returns the distance between them.

5.The code also defines a function called blinked which takes six points as input and returns an integer value indicating the state of the user's eyes. The function first calculates the distance between the upper and lower eyelids using the points passed to it. It then calculates the ratio of the upper eyelid distance to the lower eyelid distance. If the ratio is greater than 0.25, the function returns 2, indicating that the user's eyes are closed. If the ratio is between 0.21 and 0.25, the function returns 1, indicating that the user's eyes are partially closed. Otherwise, the function returns 0, indicating that the user's eyes are open.

6.The code then captures video frames from the user's webcam using OpenCV's VideoCapture function.

7.For each frame, the code converts the frame to grayscale and detects faces in the frame using the face detector.

8.For each face detected, the code draws a rectangle around the face and uses the predictor to detect the facial landmarks. It then passes the landmarks to the blinked function to determine the state of the user's eyes.

9.Based on the state of the user's eyes, the code updates the sleep, drowsy, and active counters and sets the status and color variables accordingly.

10.The code then displays the status and the frame with the facial landmarks and rectangles drawn on it using OpenCV's putText and imshow functions.

11.The code waits for the user to press the ESC key and breaks out of the loop if it is pressed
