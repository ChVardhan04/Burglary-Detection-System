This project, "Burglary-Detection-System," uses a pose detection model to identify suspicious movements in real-time through a webcam feed. Here's an overview of its components and functionality:

1. HTML Structure
   - Title and Description: The HTML displays the title “Burglary-Detection-System” and has placeholders for output messages.
   - Button: A button labeled “Start” initiates the webcam feed and begins prediction.

2. JavaScript Components
   - Libraries Used:
     - TensorFlow.js and **Teachable Machine Pose Library**: These provide tools for loading a pre-trained model, running the webcam feed, and performing real-time pose estimation and prediction.
   - Model URL: The model is hosted on Teachable Machine. This pre-trained model contains classes that represent normal and suspicious activities.

3. JavaScript Functions Explained
   - `init()`: Initializes the model, loads metadata, sets up the webcam, and attaches the webcam feed to a canvas element on the page.
   - `loop()`: Updates the webcam frame continuously and calls the `predict()` function.
   - `predict()`: Performs two main tasks:
     1. Pose Estimation: It detects the pose keypoints in the webcam frame.
     2. Classification: It classifies the pose as either “Normal” or “Suspicious” based on the model's predictions.
     - If the probability of suspicious activity is high (>= 0.98), it triggers a warning in the `output` paragraph and plays a beep sound.
   - `drawPose()`: Visualizes the pose on the canvas, showing key points and skeleton to help debug and confirm what the model is detecting in real-time.

Purpose of Each Component:
   - Teachable Machine Model: To recognize specific poses related to suspicious activities.
   - Webcam Feed: Provides real-time input to the model.
   - Pose Drawing: Visual feedback to visualize detected poses, useful in understanding the model's performance.

Working Explanation
Upon clicking "Start," the program activates the webcam feed, starts predicting poses, and classifies them. If suspicious activity is detected, it plays an alert sound and displays a warning, which is helpful for real-time burglary detection systems.
