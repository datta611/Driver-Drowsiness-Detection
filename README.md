# Driver-Drowsiness-Detection
Driver Drowsiness Detection System

Steps Of execution:
The approach would be like this:
Step 1 – To take image as input from a webcam/camera.
Step 2 – Detect the face in the image and create a Region of Interest (ROI).
Step 3 – Detect the eyes from ROI and feed it to the classifier.
Step 4 – Classifier will categorize whether eyes are open or closed.
Step 5 – Calculate score to check whether the person is drowsy.
First run training file to build a model and save it. Now load the model and run prediction file to detect the drowsiness using web cam.

