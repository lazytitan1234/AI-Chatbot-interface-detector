# Real-Time AI Chatbot Interface Detection (YOLO)

## Overview

This project implements a real-time computer vision system for detecting and classifying AI chatbot interfaces on-screen. The system is capable of identifying platforms such as ChatGPT, Gemini, and Claude using a custom-trained YOLO model.

Detected interfaces are highlighted with bounding boxes and labeled according to the identified chatbot, enabling clear visual feedback in real time.

---

## Key Features

* Real-time detection of AI chatbot interfaces
* Multi-class classification (e.g. ChatGPT, Gemini, Claude)
* Supports image, video, and screen-based input
* Visual overlay with bounding boxes and labels

---

## Technical Approach

The system leverages a YOLO-based object detection pipeline:

1. Input is captured from images, video streams, or screen recordings
2. Frames are processed using a trained YOLO model
3. Detected regions are classified into chatbot categories
4. Bounding boxes and labels are rendered on the output

The project focuses on balancing detection accuracy with performance in near real-time scenarios.

---

## Tech Stack

* Python
* YOLO (Ultralytics)
* OpenCV
* Jupyter Notebook

---

## Project Structure

```
data.yaml                  # Dataset configuration  
yolo_dataset/             # Training dataset (excluded from repo)  
runs_chatbot/             # Training outputs  
video_preds/              # Video prediction outputs  
video_preds_clean/        # Processed outputs  
img_preds/                # Image predictions  
pred_samples/             # Sample predictions  
pred_examples/            # Example outputs  
input/                    # Input data  
negatives/                # Negative samples  
backgrounds/              # Background images  
output_aug/               # Augmented data  
Task2New2.ipynb           # Training / experimentation  
Task4New2.ipynb           # Detection / evaluation  
exam_clip.mp4             # Demo video  
Pipeline Diagram.png      # System pipeline  
```

---

## Setup & Usage

### Clone the repository

git clone https://github.com/lazytitan1234/AI-Chatbot-interface-detector.git
cd YOUR-REPO

### Install dependencies

pip install -r requirements.txt

### Run the project

Use the provided Jupyter notebooks:

* `Task2New2.ipynb` for training and experimentation
* `Task4New2.ipynb` for detection and evaluation

---

## Notes on Model Files

Pre-trained weights (`.pt` files) and datasets are not included due to repository size limitations.

To run the project, you will need to:

* Download YOLO base weights (e.g. yolov8n.pt)
* Or train your own model using the provided configuration

---

## Challenges & Considerations

* Differentiating between visually similar UI layouts
* Ensuring robustness across different screen resolutions
* Balancing model accuracy with real-time performance
* Managing dataset quality and class consistency

---

## Future Improvements

* Expand dataset for improved generalization
* Add support for additional AI platforms
* Optimize inference speed for real-time deployment
* Package as a standalone desktop application

---

## Additional Context

This project was developed as part of university coursework in computer vision and reflects my interest in building practical, real-time AI systems.
