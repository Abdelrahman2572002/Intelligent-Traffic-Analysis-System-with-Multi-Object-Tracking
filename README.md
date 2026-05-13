Project Overview
This project implements a real-time multi-object tracking (MOT) pipeline for urban driving footage using YOLOv8 for per-frame detection and DeepSort for persistent ID assignment across frames. Built and evaluated on the BDD100K dataset (via Kaggle), the system annotates each track with a unique color-coded ID, motion trail, and class label, and outputs a fully annotated video alongside a statistics dashboard.

Key Features
•	YOLOv8n detection with class-filtered, confidence-thresholded detections (cars, trucks, buses, persons, bicycles, motorcycles)
•	DeepSort tracking with appearance features, Kalman filtering, and Hungarian-algorithm assignment
•	Per-track motion trails, color-coded bounding boxes, and live HUD overlay (frame count, active tracks, FPS)
•	Statistics dashboard: smoothed FPS timeline, per-class bar chart & pie chart, KPI summary cards
•	Configurable parameters: confidence threshold, max frames, frame-skip rate, tracked class whitelist

Tech Stack
Python · OpenCV · Ultralytics YOLOv8 · deep-sort-realtime · NumPy · Matplotlib · Kaggle (BDD100K)

Dataset
BDD100K — Berkeley DeepDrive 100K driving videos dataset. Available on Kaggle at:
kaggle.com/datasets/robikscube/driving-video-with-object-tracking
Quick Start
1.  Install dependencies:
pip install ultralytics deep-sort-realtime opencv-python matplotlib
2.  Set VIDEO_PATH in the config block at the top of the script.
3.  Run all cells in the Kaggle notebook (or execute the .py file directly).
4.  Output video is saved to /kaggle/working/tracked_output.mp4.

Configuration
Parameter	Default	Effect
CONF_THRESH	0.4	Raise to reduce false positives
MAX_FRAMES	None	Set e.g. 300 for a quick test run
SKIP_FRAMES	1	Set 2–3 to speed up processing
TRACK_CLASSES	6 classes	Set to None to track all COCO classes
