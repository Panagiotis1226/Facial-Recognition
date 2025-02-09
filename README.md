# Face Recognition System

This repository contains a facial recognition system implemented in Python using OpenCV and face_recognition libraries. The system consists of three main components:

## 1. Image Capture (`image_capture.py`)
This script captures training images for the facial recognition system:
- Takes photos of a person using a webcam/camera
- Saves images to a dataset folder organized by person's name
- Controls:
  - SPACE: Capture photo
  - Q: Quit capture session
- Configurable camera source (iPhone/Immersed/Webcam)
- Captures high resolution (1920x1080) images

## 2. Model Training (`model_training.py`) 
This script processes the captured images and creates facial encodings:
- Loads all images from the dataset folder
- Detects faces using HOG model
- Generates facial encodings for each detected face
- Saves encodings to `encodings.pickle` file for later use
- Associates encodings with person names

## 3. Facial Recognition (`facial_recognition.py`)
Real-time facial recognition system with the following features:
- Loads pre-trained facial encodings
- Performs real-time face detection and recognition
- Displays:
  - Bounding boxes around detected faces
  - Name labels with confidence scores
  - FPS counter
- Controls:
  - Q: Quit program
- Performance optimization:
  - Configurable frame scaling
  - RGB/BGR color space handling
  - Confidence score calculation

## Requirements
- Python 3.x
- OpenCV (`cv2`)
- face_recognition
- numpy
- imutils
- pickle

## Usage
1. Capture training images:
   ```bash
   python image_capture.py
   ```
2. Train the model:
   ```bash
   python model_training.py
   ```
3. Run facial recognition:
   ```bash
   python facial_recognition.py
   ```
