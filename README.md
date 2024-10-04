Here's a more detailed **README** file structure for your **AwareDrive** project that is suitable for GitHub:

---

# AwareDrive - Driver Drowsiness Detection System

AwareDrive is a real-time driver drowsiness detection system designed to enhance road safety by monitoring the driver's face and alerting them when signs of drowsiness are detected. Built using the YOLOv5 model for object detection and a Tkinter-based GUI, AwareDrive integrates a live camera feed with customizable alarm functionality to provide users with a seamless experience.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [Technology Stack](#technology-stack)
- [How It Works](#how-it-works)
- [Screenshots](#screenshots)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Real-time Drowsiness Detection**: Uses YOLOv5 for real-time detection of drowsy behavior.
- **Live Video Feed**: Displays the live camera feed in a user-friendly interface.
- **Adjustable Sensitivity**: Users can adjust the detection threshold using built-in buttons to suit different scenarios.
- **Customizable Alerts**: Users can choose and set their own audio alert files (e.g., .wav or .mp3) for notifications.
- **Counter Reset**: Automatically resets the drowsiness detection counter after reaching the threshold and sounding an alert.
- **Modular and Extensible**: Built with modular code that allows for easy modifications and improvements.

## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)
- [YOLOv5](https://github.com/ultralytics/yolov5) weights (custom trained model required)
- Webcam for live video feed

### Required Python Libraries
Install the required dependencies by running the following command:
```bash
pip install torch opencv-python-headless customtkinter numpy Pillow python-vlc
```

### Clone the Repository
Clone the AwareDrive project repository to your local machine:
```bash
git clone https://github.com/your-username/AwareDrive.git
cd AwareDrive
```

### Download YOLOv5 Weights
Place your custom YOLOv5 weights file in the following directory:
```bash
yolov5/runs/train/exp5/weights/last.pt
```

## Usage

To start the AwareDrive application, simply run the following command:
```bash
python awaredrive.py
```

The app window will display the live video feed from your webcam. As the app detects drowsiness, it will trigger an alarm once the detection threshold is exceeded. You can adjust the sensitivity of the detection using the buttons in the app.

## Customization

### Adjusting Detection Sensitivity
The app provides buttons to increase or decrease the counter limit for detection:
- **Increase Counter**: Raises the threshold at which drowsiness is detected.
- **Decrease Counter**: Lowers the threshold to make detection more sensitive.

### Changing Alert Sounds
You can select your own custom alert sounds via the file browser integrated in the GUI. Supported formats include `.wav` and `.mp3`.

## Technology Stack
- **Detection**: YOLOv5 (PyTorch)
- **Video Capture**: OpenCV
- **GUI**: Tkinter and customTkinter
- **Audio**: VLC media player integration for playing audio alerts
- **Image Processing**: PIL (Python Imaging Library)

## How It Works

1. **Live Camera Feed**: AwareDrive captures a continuous video feed from the webcam using OpenCV.
2. **YOLOv5 Model**: The YOLOv5 model processes each frame to detect facial features that suggest drowsiness (e.g., closed eyes).
3. **Drowsiness Detection**: When the driver is detected as drowsy for a prolonged period (customizable via counter), an alarm is triggered.
4. **Custom Alerts**: Users can upload custom sound files to be played as alerts when drowsiness is detected.
5. **Reset Counter**: The detection counter automatically resets after an alarm has been triggered, ensuring no continuous false positives.

## Screenshots

![Screenshot 2024-04-25 214551](https://github.com/user-attachments/assets/a3422724-f703-47c7-ada1-c05d36d9ad3f)

