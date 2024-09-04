# Real-Time Hand Tracking and Virtual Mouse Control System
This project is a real-time computer vision application that tracks hand movements using a webcam and allows control of the computer's mouse through hand gestures. It leverages MediaPipe for hand detection and tracking, providing a virtual mouse experience without the need for any physical input devices.

![mouse](https://github.com/user-attachments/assets/ee8d6268-7a13-47ea-8af5-34f9ed05ea4a)

![mouse2](https://github.com/user-attachments/assets/ca80b66f-fe17-4349-829f-14902327e1a0)

## 1. Real-Time Hand Detection and Tracking
The application uses a webcam feed (cv2.VideoCapture(0)) to capture live video frames of the user's hands.

It utilizes the MediaPipe library to detect and track hand landmarks in real-time, drawing connections between hand joints.
## 2. Hand Tracking with Custom Hand Detector
A custom class handDetector is implemented to handle hand detection, landmark tracking, and various calculations.

Key functionalities include finding hand positions, determining which fingers are up, and calculating distances between specific landmarks for gesture recognition.
## 3. Virtual Mouse Control
The application controls the mouse cursor by detecting the positions of the index and middle fingers.

If only the index finger is up, the mouse moves according to the index finger's position on the screen.

When both the index and middle fingers are up, the application enters clicking mode, and a mouse click is triggered when the distance between these fingers is short enough.
## 4. Smoothing and Calibration
The system employs a smoothing mechanism to ensure smoother and more precise cursor movements.

Frame reduction is used to calibrate the hand detection region, making the virtual mouse control experience more intuitive and user-friendly.
## 5. Hand Distance Calculation
The application calculates the distance between fingertips (e.g., index and middle fingers) using Euclidean distance.

This information is used to determine actions such as mouse clicks, enhancing the interactivity of the virtual mouse control.
## 6. Application Flow
Hand Detection: Detects hand landmarks in real-time using MediaPipe.

Gesture Recognition: Identifies which fingers are up and calculates distances between key landmarks.

Mouse Movement: Maps the index finger position to screen coordinates, allowing control of the cursor.

Click Detection: Triggers mouse clicks based on finger proximity, simulating left-click actions.
## Use Case
This project is ideal for interactive presentations, touchless control systems, or accessibility applications where traditional input devices are impractical.

It provides a novel way to interact with a computer using only hand gestures, making it suitable for creative and practical purposes.

Note: I do not own the copyrights of this project.(youtube @murtazasworkshop) It is for learning purposes only.
