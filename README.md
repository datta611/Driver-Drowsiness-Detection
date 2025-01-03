# Driver-Drowsiness-Detection

Driver Drowsiness Detection System

## Project Structure

Driver-Drowsiness-Detection/
- eyes/ # Contains eye detection Haar cascade files
- haar cascade files/ # Contains Haar cascade files for face detection
- models/ # Contains saved models
- alarm.wav # Alarm sound file for drowsiness detection
- Model Training.ipynb # Jupyter Notebook for model training
- Prediction.ipynb # Jupyter Notebook for drowsiness detection
- README.md # Documentation of the project

## Overview

This project implements a Driver Drowsiness Detection System that identifies whether a driver is drowsy based on eye status and alerts the user.

## Steps of Execution

The approach follows these steps:

1. **Image Input**:

   - Capture images from a webcam or camera.

2. **Face Detection**:

   - Detect the face in the image using Haar cascade classifiers.
   - Create a Region of Interest (ROI) around the face.

3. **Eye Detection**:

   - Detect eyes within the ROI using Haar cascade files.
   - Preprocess the detected eyes to feed them into a classifier.

4. **Classification**:

   - Use a trained machine learning model to classify whether the eyes are open or closed.

5. **Drowsiness Detection**:
   - Calculate a score based on the duration the eyes remain closed.
   - Trigger an alarm (using `alarm.wav`) if the driver is detected as drowsy.

## Files and Usage

1. **Model Training.ipynb**:

   - This file is used for training the model that classifies whether eyes are open or closed.
   - Ensure the dataset for training is properly loaded and the trained model is saved in the `models/` directory.

2. **Prediction.ipynb**:

   - This file uses the trained model to predict drowsiness in real-time.
   - Connect a webcam for live detection.
   - The program detects drowsiness and plays an alarm when necessary.

3. **alarm.wav**:

   - An audio file used to alert the driver when drowsiness is detected.

4. **eyes/**:

   - Contains Haar cascade files specifically for eye detection.

5. **haar cascade files/**:

   - Contains Haar cascade files for face detection, enabling efficient ROI creation.

6. **models/**:
   - Contains the trained models used for eye classification.

## How to Run

1. **Train the Model**:

   - Open the `Model Training.ipynb` file.
   - Run all the cells to train the model.
   - Ensure the trained model is saved in the `models/` directory.

2. **Run Prediction**:

   - Open the `Prediction.ipynb` file.
   - Ensure the webcam is connected.
   - Load the trained model from the `models/` directory.
   - Run the cells to start real-time drowsiness detection.

3. **Dependencies**:
   - Ensure the following libraries are installed:
     - OpenCV
     - Numpy
     - Matplotlib
     - Any additional libraries required in the Jupyter Notebooks.

## Notes

- Make sure the webcam is functional and permissions are granted.
- Place Haar cascade files in the respective directories for face and eye detection.
- The alarm sound (`alarm.wav`) should be loud enough to alert the driver.

## Future Improvements

- Improve the accuracy of the classifier.
- Extend functionality for multi-driver detection.
- Integrate the system into a real-time driving environment with minimal computational resources.

Feel free to contribute and enhance this project!
