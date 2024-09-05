**Real-Time PPE Safety Kit Detection Using YOLOv8**

**Overview**

This project implements a real-time Personal Protective Equipment (PPE) detection system using the YOLOv8 algorithm. The goal is to identify whether individuals are wearing the necessary safety equipment, such as helmets, vests, and gloves, in an industrial or construction environment. The model processes live video feeds or recorded footage, detecting the presence and correct usage of PPE to enhance workplace safety.

**Features**

- Real-time detection of multiple PPE items, such as helmets, vests, and gloves.
- High-speed inference using the YOLOv8 algorithm.
- Works with live video streams or recorded footage.
- Easily scalable to detect additional safety gear.
- Provides alerts when non-compliance with safety regulations is detected.

**Dataset**

The dataset used for this project consists of images of people in industrial environments, labeled with bounding boxes for various PPE items, including:

- Helmets
- Safety vests
- Gloves
- Protective goggles

**Sources:**
- Custom images from industrial sites.
- Public datasets such as the [https://universe.roboflow.com/test-uooq1/ppe-factory-bmdcj] and others relevant to PPE detection.

**Model**

We use the YOLOv8 (You Only Look Once version 8) object detection algorithm, which offers a balance between speed and accuracy, making it ideal for real-time applications. YOLOv8 uses a single neural network to predict bounding boxes and class probabilities directly from full images in a single evaluation, making it faster than two-stage object detectors.

**Why YOLOv8?**
- Real-Time Performance: YOLOv8 is optimized for real-time processing, with faster inference speed compared to earlier versions.
- High Accuracy: YOLOv8 provides improved accuracy over its predecessors, making it suitable for safety-critical applications.
- Modular Design: YOLOv8 can be easily fine-tuned for new PPE detection categories.

**Installation**

**Prerequisites**

- Python 3.8+
- CUDA-enabled GPU (for faster training and inference)
- PyTorch (with GPU support)
- OpenCV
- Ultralytics YOLOv8 package

**Real-Time Detection**

To run detection on a live webcam feed: python detect.py --source 0 --weights yolov8n.pt

**Results**

The system outputs bounding boxes and class labels (Helmet, Vest, Gloves, etc.) around detected objects in real-time. Alerts are generated if required PPE is missing.

**License**

This project is licensed under the MIT License. See the LICENSE file for details.

**Acknowledgments**

Ultralytics for developing YOLOv8.
OpenCV and PyTorch communities for their excellent libraries and tools.
Industrial sites and dataset providers for making this project possible.
