# Gesture Recognition 🖐️

> Real-time hand gesture classification using DepthAI, MediaPipe, and OpenCV.

## Overview

A real-time gesture recognition system built using **DepthAI**, **MediaPipe**, and **OpenCV**. The camera stream is processed to detect hand landmarks and classify gestures including Open Palm, Thumbs Up, OK Sign, Point Forward, and Wave. A temporal buffer tracks wrist motion to reliably detect waving gestures.

The project demonstrates practical computer vision, spatial analysis, and intuitive touch-free interaction suitable for robotics and IoT interfaces.

## Supported Gestures

| Gesture | Description |
|---|---|
| ✋ Open Palm | All fingers extended and spread |
| 👍 Thumbs Up | Thumb up, other fingers closed |
| 👌 OK Sign | Thumb and index forming a circle |
| 👆 Point Forward | Index finger extended, others closed |
| 👋 Wave | Wrist motion detected via temporal buffer |

## Features

- 🖐️ **21-Point Hand Landmark Detection** — Full hand skeleton tracking via MediaPipe
- 🧠 **Rule-Based Classifier** — Fast, lightweight gesture classification without heavy ML inference
- 🌊 **Wave Detection** — Temporal buffer tracks wrist trajectory for motion-based gestures
- 📡 **DepthAI Pipeline** — Spatial awareness and efficient camera processing
- ⚡ **Real-Time Performance** — Low-latency inference on edge hardware

## System Architecture

```
OAK-D Camera (DepthAI)
    ↓
Frame Capture + Preprocessing
    ↓
MediaPipe Hand Landmark Detection (21 keypoints)
    ↓
Landmark Analysis & Finger State Extraction
    ↓
Gesture Classifier → { Palm, Thumbs Up, OK, Point, Wave }
    ↓
Temporal Buffer (for Wave)
    ↓
Output Display / Action Trigger
```

## Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3 |
| Hand Tracking | MediaPipe Hands |
| Camera Pipeline | DepthAI (OAK-D) |
| Computer Vision | OpenCV |
| Hardware | OAK-D / Raspberry Pi |

## Project Structure

```
Gesture-Recognition/
├── main.py                  # Main application loop
├── gesture_classifier.py    # Landmark-based gesture rules
├── wave_detector.py         # Temporal wrist motion buffer
├── pipeline.py              # DepthAI camera pipeline
├── utils/
│   └── visualiser.py        # Overlay rendering
├── requirements.txt
└── README.md
```

## Getting Started

### Prerequisites

```bash
pip install opencv-python mediapipe depthai numpy
```

### Run

```bash
python main.py
```

## Results

- ✅ Reliable classification of 5 distinct gestures
- ✅ Wave detection using temporal wrist trajectory
- ✅ Real-time performance at 20+ FPS on edge hardware

## Applications

- 🤖 Touchless robot control interfaces
- 🏠 Smart home gesture controls
- ♿ Accessibility input systems
- 🎮 Interactive installations

## Skills Demonstrated

`Python` · `MediaPipe` · `OpenCV` · `DepthAI` · `Gesture Recognition` · `Computer Vision` · `Spatial AI`
