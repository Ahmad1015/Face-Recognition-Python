# Face Recognition Using IP Camera or Webcam in Real Time

This project demonstrates a real-time face recognition system using an IP camera stream. The system captures video frames, detects faces, and recognizes known faces using the `face_recognition` library and OpenCV.

## Features

- Real-time face detection and recognition using an IP camera.
- Identification of known faces.
- Display of recognized names on the video stream.

## Prerequisites

Before running the project, make sure you have the following installed:

- Python 3.x
- OpenCV
- Numpy
- face_recognition

### Installation

You can install the required libraries using pip:

```bash
pip install numpy opencv-python face_recognition
```
## How to Use
### Prepare a Known Image

- Place a known image of the person you want to recognize in the same directory as the script. The image should be named Official_photo.jpeg by default.
### Configure the IP Camera
- Using an IP Camera:
Ensure your IP camera is connected and streaming. Update the IP address and port in the video_capture URL to match your camera's configuration:
```python
video_capture = cv2.VideoCapture("http://192.168.10.6:4747/video")
```
- Using a Webcam:
You can also use your webcam by replacing the IP address with 0:
```python
video_capture = cv2.VideoCapture(0)
```
### Run the Script
- Execute the script using Python:
```python
python face_recognition.py
```
- The script will open a window displaying the video stream with face detection and recognition. If a known face is detected, the person's name will appear below the detected face.

### Exit the Application
- Press the 'q' key on the keyboard to stop the video stream and exit the application.

### References
- [face_recognition GitHub Repository](https://github.com/ageitgey/face_recognition)
