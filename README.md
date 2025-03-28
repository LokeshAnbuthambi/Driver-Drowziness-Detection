# Drowsiness and Distraction Detection System

This project is a real-time Drowsiness and Distraction Detection System that monitors the driver's state through a webcam feed. It detects drowsiness by calculating the Eye Aspect Ratio (EAR) and alerts the user with a sound if drowsiness is detected. It also monitors distraction by analyzing head pose and triggers an alert if the driver is looking away from the road.

# Features
Real-time eye blink detection to monitor drowsiness.
Head pose estimation to detect driver distraction.
Audio alerts to warn the driver when drowsy or distracted.
Uses OpenCV and Dlib for image processing and facial landmark detection.
Lightweight and efficient for real-time applications.

# Technologies Used
Python
OpenCV
Dlib
NumPy
SciPy
Winsound (Windows-specific)

# Install the required libraries:
pip install opencv-python dlib numpy scipy
Download the pre-trained shape predictor file (shape_predictor_68_face_landmarks.dat) from Dlib Model Zoo and place it in the project directory.

# Usage
## Run the script:
python drowsiness_detector.py
The webcam feed will open, and the system will start monitoring drowsiness and distraction.
Press 'q' to exit the program.

# Configuration
Adjust the following parameters as needed:
EAR_THRESHOLD: Minimum Eye Aspect Ratio to trigger drowsiness alert.
FRAME_THRESHOLD: Minimum consecutive frames with low EAR to raise an alert.
HEAD_TILT_THRESHOLD: Maximum head tilt angle before triggering distraction alert.

# How It Works
The system captures video from the webcam and converts it to grayscale for processing.
Dlib's pre-trained face detector locates the face in the frame.
Facial landmarks are identified, and the Eye Aspect Ratio (EAR) is calculated.
If EAR drops below a threshold for a specified duration, a drowsiness alert is triggered.
Head pose estimation is performed to detect driver distraction.

# Output
Visual alerts on the webcam feed.
Audio alerts when drowsiness or distraction is detected.

# Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

# Acknowledgments
Dlib for face detection and landmark prediction.
OpenCV for real-time video processing.
Scipy and NumPy for numerical calculations.
