# Real-Time Traffic Sign Detection 🚦

## Abstract

This project performs **real-time traffic sign detection and classification** using a deep learning based object detection model.

The system detects traffic signs in images, videos, and live camera feeds. Each detected traffic sign is enclosed inside a **bounding box**, and the predicted **class label** is displayed above the object.

The model is based on the **YOLOv5 small object detection architecture**, optimized for real-time performance.

The model was trained on **3000 manually labeled images** across **61 traffic sign classes** and achieved:

* **91.75% mAP@0.5**
* **Real-time performance of ~45 FPS** on NVIDIA GeForce MX250 GPU

This project demonstrates how deep learning can be used for **autonomous driving systems, intelligent transportation, and driver assistance applications**.

---

# Project Repository

GitHub Repository:

https://github.com/0ye0m/Real-Time-Traffic-Sign-Detection

---

# How to Run the Project

## 1. Download the Repository

Clone the repository or download the ZIP file.

```
git clone https://github.com/0ye0m/Real-Time-Traffic-Sign-Detection.git
```

Navigate into the project directory.

---

## 2. Extract Model Files

Inside the main project folder locate:

```
Models.zip
```

Extract it so that the directory structure becomes:

```
Model/
   weights/
      best.pt
```

This file contains the **trained YOLOv5 model weights**.

---

## 3. Install Dependencies

Install all required libraries using:

```
pip install -r requirements.txt
```

If using Anaconda:

```
conda install --file requirements.txt
```

---

## 4. Navigate to Code Directory

```
cd Codes
```

---

# Running Traffic Sign Detection

## Detect Traffic Signs in an Image

Place your image inside the **Test** folder.

Example:

```
Test/test.jpg
```

Run:

```
python detect.py --source ../Test/test.jpg
```

---

## Detect Traffic Signs in a Video

Place a video file inside the **Test** folder.

Example:

```
Test/video.mp4
```

Run:

```
python detect.py --source ../Test/video.mp4
```

---

## Real-Time Detection Using Webcam

To detect traffic signs from a live camera feed:

```
python detect.py --source 0
```

---

# Output

Detection results are automatically saved inside the:

```
Results/
```

directory.

Each output image or video will contain:

* Bounding boxes
* Predicted traffic sign label
* Confidence score

---

# Project Directory Structure

```
Real-Time-Traffic-Sign-Detection
│
├── Codes
│   ├── models
│   └── utils
│
├── Model
│   └── weights
│
├── Results
│
├── Sample Dataset
│
└── Test
```

---

# Example Results

The system detects multiple traffic signs simultaneously and classifies them accurately in real time.

Features include:

* Bounding box localization
* Multi-class detection
* Real-time inference

The model performs robust detection even when the vehicle is moving at high speed.

Typical performance ranges between:

**28 – 38 FPS in real-time detection scenarios.**

---

# Applications

This project can be used in:

* Autonomous Driving Systems
* Advanced Driver Assistance Systems (ADAS)
* Smart Traffic Monitoring
* Self-driving vehicle research
* Computer Vision learning projects

---

# References

1. YOLOv5 Object Detection Framework
   https://github.com/ultralytics/yolov5

2. Road Sign Dataset (Kaggle)
   https://www.kaggle.com/andrewmvd/road-sign-detection

3. YOLO Research Paper
   https://arxiv.org/pdf/1506.02640.pdf

4. LabelImg Annotation Tool
   https://github.com/tzutalin/labelImg
