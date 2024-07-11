# DrowsinessDetection
. 
This is an implementation of a drowsiness detection system using OpenCV, Keras, and Pygame libraries. It uses a pre-trained convolutional neural network (CNN) model to classify whether the person's eyes are open or closed.

Here's a breakdown of the code:

1. Importing the necessary libraries:
   - `cv2` for computer vision tasks
   - `os` for interacting with the operating system
   - `keras.models` for loading the pre-trained CNN model
   - `numpy` for numerical computations
   - `pygame.mixer` for playing audio
   - `time` for managing time-related operations

2. Initializing Pygame and loading the alarm sound file.

3. Loading the Haar cascade classifiers for face detection and eye detection.

4. Defining the labels for eye status.

5. Loading the pre-trained CNN model.

6. Getting the current working directory and initializing the video capture.

7. Defining some variables for counting frames, score, and drawing rectangles.

8. Starting the main loop to read frames from the video capture.

9. Converting the frame to grayscale.

10. Detecting faces, left eyes, and right eyes in the grayscale frame using the Haar cascades.

11. Drawing rectangles around the detected faces.

12. Processing the right eye region:
    - Extracting the region of interest (ROI) from the frame.
    - Preprocessing the ROI for input to the CNN model.
    - Predicting the eye status (open or closed) using the model.
    - Updating the label accordingly.

13. Processing the left eye region:
    - Extracting the ROI from the frame.
    - Preprocessing the ROI for input to the CNN model.
    - Predicting the eye status.
    - Updating the label accordingly.

14. Checking the eye status predictions and updating the score accordingly.

15. Displaying the score on the frame.

16. If the score exceeds a certain threshold (15 in this case), indicating drowsiness:
    - Saving the frame as an image.
    - Playing the alarm sound.

17. Drawing a rectangle around the frame if drowsiness is detected.

18. Displaying the frame.

19. Breaking the loop if the 'q' key is pressed.

20. Releasing the video capture and destroying the OpenCV windows.

