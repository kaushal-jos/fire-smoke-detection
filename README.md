# Fire & Smoke Detection System

## Project Overview

- This project implements a real time fire and smoke detection system using surveillance footage captured from an IP webcam. It leverages state of the art Deep Learning models (YOLOv8) and OpenCV for video processing to detect significant fire and smoke incidents, while intelligently filtering out false positives from small, harmless sources such as gas stoves, lighters, and candles.

- The system is designed to trigger timely alerts upon detecting critical fire or smoke events, making it suitable for enhancing safety in homes, offices, warehouses, and public spaces.

## Features

- **Real time detection** of fire and smoke from live surveillance footage.
- **False positive filtering** to ignore small, non hazardous fire / smoke sources.
- **Alert mechanism** with sound notifications on Windows systems.
- Utilizes **YOLOv8** for accurate and fast object detection.
- Easy integration with any IP webcam streaming snapshot images.

## Getting Started

### Prerequisites

- Compatible Python version: >= 3.8, < 3.13 (recommended: 3.10.x or 3.11.x)

- An IP Webcam app or IP camera that streams snapshot images via HTTP

- Windows OS (for sound alert support; for other OS, modify alert part)

### Installation

1. Clone the repository
2. Create and activate a virtual environment 
3. Install the required packages
4. Download or place your trained YOLOv8 weights file (`fire_smoke_yolov8s.pt`) into the project folder.

### Configuration

- Update the IP camera URL in the script (`main.py`) :
  `URL = "http://<your-ip-address>:8080/shot.jpg"`
- Adjust detection confidence thresholds and filtering parameters (if needed).

### Running the Project

- Run the main detection script: `python main.py`
- Press `ESC` to exit the real time detection window.
