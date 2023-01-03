# Driver-Drowsiness-Detection
Driver drowsiness detection is a project built using Dlib and OpenCV with Python as a backend language.<br>

This code is using computer vision to detect whether a person's eyes are open or closed, and is using that information to determine whether the person is sleeping, drowsy, or active. It does this by using dlib, a machine learning library, to detect a face in the frame of a video and to predict the positions of facial landmarks, such as the corners of the eyes and mouth. It then uses these landmarks to compute the ratio of the distance between the upper and lower eyelids and the distance between the eyebrows and the lower eyelid, and based on this ratio it determines whether the person's eyes are open or closed. If the person's eyes are closed for a certain number of frames in a row, the code increments a counter and if the counter exceeds a certain threshold it plays an alarm sound and displays a message on the screen indicating that the person is sleeping, drowsy, or active.<br>
<h3>The algorithm outlines are :</h3>
1.Initialize a video capture object and a dlib face detector and predictor.<br>
2.Initialize counters for sleep, drowsiness, and activity. Initialize the status message and color to empty strings and black, respectively.<br>
3.Start a loop to process each frame of the video:<br>
    1.Capture a frame from the video.<br>
    2.Convert the frame to grayscale.<br>
    3.Detect faces in the frame using the face detector.<br>
    4.For each face:<br>
        1.Draw a rectangle around the face.<br>
        2.Predict the facial landmarks for the face.<br>
        3.Compute the ratio of the distances between the upper and lower eyelids and the distance between the eyebrows and the lower eyelid for each eye.<br>
        4.If both eyes are fully closed:<br>
             1.Increment the sleep counter.<br>
             2.Reset the drowsiness and activity counters.<br>
             3.If the sleep counter exceeds a threshold:<br>
                 1.Update the status message to "SLEEPING!!!".<br>
                 2.Update the color to red.<br>
                 3.Play the sleep alarm sound.<br>
         5.If one eye is partially closed:<br>
             1.Increment the drowsiness counter.<br>
             2.Reset the sleep and activity counters.<br>
             3.If the drowsiness counter exceeds a threshold:<br>
                 1.Update the status message to "Drowsy!".<br>
                 2.Update the color to blue.<br>
                 3.Play the drowsiness alarm sound.<br>
          6.If both eyes are fully open:<br>
              1.Increment the activity counter.<br>
              2.Reset the sleep and drowsiness counters.<br>
              3.If the activity counter exceeds a threshold:<br>
                  1.Update the status message to "Active :)".<br>
                  2.Update the color to green.<br>
     5.Display the status message and color on the frame.<br>
     6.Display the frame.<br>
4.Release the video capture object.<br>



