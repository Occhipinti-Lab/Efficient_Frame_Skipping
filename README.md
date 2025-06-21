# efficient-video-processing-autonomous-driving

# 🚗 Efficient Frame Skipping for Computational Load Reduction in Autonomous Lane and Object Detection

This project presents a hybrid deep learning-based video processing pipeline aimed at reducing computational load in autonomous driving systems by efficiently skipping redundant frames during lane and object detection. The framework integrates lane detection, object detection, and a SlowFast network-based temporal modeling technique, optimized with an Absolute Pixel Difference (APD) strategy.

---

## 🔍 Motivation

Autonomous driving systems must process continuous video streams in real-time, demanding high computational power. Many frames in such videos are visually similar, especially in low-motion scenarios. This project addresses that inefficiency by introducing a frame-skipping mechanism based on pixel-level similarity — helping conserve computational resources without compromising detection accuracy.

---

## 🧠 Key Features

- **Hybrid Processing Pipeline** combining traditional computer vision and deep learning.
- **Efficient Frame Skipping** using Absolute Pixel Difference (APD) to reduce redundant computation.
- **Dual-path SlowFast Network Preparation** for temporal consistency and multi-scale analysis.
- **Integrated Lane Detection** using Canny edge detection and Hough Line Transform.
- **Real-time Object Detection** with YOLOv5.
- **Dynamic Output Generation** with highlighted lanes, bounding boxes, and optimized FPS.

---

## ⚙️ Pipeline Overview

### ✅ Step 1: Environment Setup
- Install required libraries: OpenCV, PyTorch, and YOLOv5.
- Import modules for motion analysis, lane detection, and video rendering.

### ✅ Step 2: Lane Detection
- Apply **Canny Edge Detection** and **Hough Line Transform** to extract lane lines.
- Enhances frames by highlighting lane boundaries.

### ✅ Step 3: Object Detection
- Use **YOLOv5** to detect vehicles, pedestrians, and traffic signs.
- Annotate objects with bounding boxes, class names, and confidence scores.

### ✅ Step 4: Frame Similarity Analysis
- Calculate **Absolute Pixel Difference** between consecutive frames.
- Skip frames with minimal changes using an adaptive threshold.

### ✅ Step 5: SlowFast Input Preparation
- Generate inputs for SlowFast network:
  - **Fast Pathway** for fine-grained motion
  - **Slow Pathway** for coarse temporal features

### ✅ Step 6: Video Processing Workflow
- Apply all processing steps frame-by-frame.
- Skip similar frames and write meaningful frames to output video.

### ✅ Step 7: Performance Metrics
- Display:
  - Total processed frames
  - Skipped frame percentage
  - Frame rate (FPS)

### ✅ Step 8: Dynamic Output Generation
- Save final video with:
  - Highlighted lane lines
  - Labeled bounding boxes
  - Adaptive frame rate for efficient playback

---

## 📈 Results & Applications

- Reduced computational cost by skipping redundant frames
- Maintained detection accuracy and temporal awareness
- Applications include:
  - Real-time traffic monitoring
  - Embedded systems in autonomous vehicles
  - Edge-based video analytics

---

## 🏁 Future Enhancements

- Integrate object tracking (e.g., Deep SORT) for better temporal continuity
- Extend to multi-camera support for urban scenarios
- Deploy on edge devices using TensorRT or ONNX for real-time performance

---

## 📸 Sample Output


_A processed video frame with lane lines, object labels, and frame skipping applied video is available in 'Data/Output' folder._

---



