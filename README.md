# YOLO-Person-Detection-Pipeline
# 🎯 SnapTrack: YOLOv8 Person Detection Pipeline

A custom video-to-frame-to-detection pipeline built for efficient person detection using YOLOv8. This modular workflow takes raw videos (e.g., from YouTube), trims them into 15-second clips, extracts frames at 5 FPS, and feeds them into a YOLOv8 model for high-accuracy person detection.

---

## 🔧 Project Components Summary

### 📁 `Raw_Movie_Demo.zip`
- Contains original, **uncut** videos (e.g., downloaded from YouTube).
- These are **unannotated** and act as the **master source videos**.

---

### 🛠️ `video_cutter.ipynb`
- A custom Jupyter notebook for trimming videos into **15-second segments**.
- **Input**: Videos from `Raw_Movie_Demo.zip`.
- **Output**: Short clips saved into `videos.zip`.

---

### 📁 `videos.zip`
- Compressed folder containing all **15-second videos**, ready for frame extraction.
- These shorter clips improve processing efficiency and training performance.

---

### 🖼️ `frame_extractor.ipynb`
- Extracts **frames at 5 FPS** from the shortened videos.
- **Input**: Videos from `videos.zip`.
- **Output**: Frame images stored in a `frames/` directory.

---

### 📁 `frames_5fps.zip`
- Contains **1,507 extracted images** for training and annotation.
- Packaged for easy upload to platforms like **Roboflow**.

---

### 🤖 `yolov8.ipynb`
- Master notebook for **YOLOv8-based person detection**.
- Trained on frames from `frames_5fps.zip`.
- Includes:
  - Detection visualizations.
  - IOU score of **0.7** indicating high accuracy.
  - Image samples showing model performance.

---

## 📈 Workflow Overview

1. 🎥 Collect raw videos → `Raw_Movie_Demo.zip`  
2. ✂️ Trim videos to 15s → `video_cutter.ipynb` → `videos.zip`  
3. 🖼️ Extract frames at 5 FPS → `frame_extractor.ipynb` → `frames_5fps.zip`  
4. 📤 Upload to Roboflow or annotate  
5. 🤖 Train or test using → `yolov8.ipynb`

---

## 🚀 Features

- Modular and customizable video processing
- High-speed frame extraction (5 FPS)
- YOLOv8 person detection with solid performance
- Ready for integration with annotation tools (e.g., Roboflow)

---

## 🧠 Requirements

Make sure you have the following (or similar) tools/libraries installed:

- Python 3.8+
- OpenCV
- Ultralytics YOLOv8
- Jupyter Notebook
- ffmpeg (for video trimming)
- Roboflow SDK (optional)

