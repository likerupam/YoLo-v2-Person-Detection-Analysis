# YOLOv2 Person Detection Error Analysis

**Course:** ML System Optimization / Computer Vision\
**Assignment:** Detection Error Analysis using YOLOv2\
**Student:** Rupam Mahato\
**Roll No:** 2024CT05038

------------------------------------------------------------------------

## 📌 Project Overview

This project analyzes **YOLOv2-based person detection** on
self-collected real-world images. The goal is to evaluate detection
performance through:

-   True Positives (TP)
-   False Positives (FP)
-   False Negatives (FN)
-   Intersection over Union (IoU)
-   Precision and Recall metrics

------------------------------------------------------------------------

## 🎯 Objective

-   Apply YOLOv2 to detect persons in real-world images
-   Manually create ground truth annotations
-   Compare predicted bounding boxes with ground truth using IoU
-   Analyze detection errors (TP, FP, FN)
-   Compute evaluation metrics such as Precision and Recall

------------------------------------------------------------------------

## 📂 Dataset

-   Images are self-collected in various environments (offices, outdoor
    spaces, malls, public areas).
-   All images are original and captured by the student.
-   Google Drive link for images is included inside the notebook.

------------------------------------------------------------------------

## ⚙️ Model Details

-   Model Used: YOLOv2
-   Confidence Threshold: 0.5
-   IoU Threshold: 0.5
-   Classes: COCO dataset classes
-   Implementation: OpenCV DNN module

------------------------------------------------------------------------

## 🧠 Methodology

### 1️⃣ Import Required Libraries

-   OpenCV\
-   NumPy\
-   Matplotlib\
-   Pathlib\
-   OS utilities

### 2️⃣ Load Images

Images from the Source Images folder are loaded and displayed.

### 3️⃣ YOLOv2 Detection

-   Load weights, config, and class names.
-   Perform person detection.
-   Extract bounding boxes and confidence scores.

### 4️⃣ Ground Truth Creation

Manual bounding boxes are created for actual persons in each image.

### 5️⃣ IoU Calculation

IoU = Area of Overlap / Area of Union

Detection classification: - TP if IoU \> 0.5 - FP if no matching ground
truth exists - FN if a ground truth person is not detected

------------------------------------------------------------------------

## 📊 Evaluation Metrics

Precision = TP / (TP + FP)

Recall = TP / (TP + FN)

------------------------------------------------------------------------

## 📊 Observations

-   Performs well in clear lighting and frontal poses.
-   Performance drops in occlusion, small objects, low light, and
    complex backgrounds.
-   Threshold tuning impacts precision-recall trade-off.

------------------------------------------------------------------------

## 🚀 How to Run

1.  Install dependencies: pip install opencv-python numpy matplotlib

2.  Ensure YOLOv2 weights, config, coco.names, and Source Images folder
    are present.

3.  Run: jupyter notebook

------------------------------------------------------------------------

## 📁 Recommended Folder Structure

CV_Assignment_2\_Rupam_Mahato.ipynb\
Source_Images/\
models/\
├── yolov2.weights\
├── yolov2.cfg\
└── coco.names\
README.md

------------------------------------------------------------------------

## 🏁 Conclusion

This project demonstrates real-world object detection evaluation,
highlighting error analysis, IoU-based validation, and precision-recall
trade-offs.
