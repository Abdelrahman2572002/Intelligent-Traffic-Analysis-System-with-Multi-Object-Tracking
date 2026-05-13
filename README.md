Project Overview
This project implements a real-time multi-object tracking (MOT) pipeline for urban driving footage using YOLOv8 for per-frame detection and DeepSort for persistent ID assignment across frames. Built and evaluated on the BDD100K dataset (via Kaggle), the system annotates each track with a unique color-coded ID, motion trail, and class label, and outputs a fully annotated video alongside a statistics dashboard.

✨ Features
🎯 Real-time object detection using YOLOv8
🧠 Multi-object tracking with DeepSORT
🆔 Persistent ID assignment for each object
🛣️ Trajectory visualization (motion trails)
📊 Class-wise detection statistics
⚡ FPS monitoring for performance evaluation
🎥 Output annotated video generation
🧠 What This Project Does
Detects vehicles and pedestrians in video frames
Tracks each object across time with a unique ID
Draws movement paths (trajectories)
Measures system performance (FPS, counts, etc.)
Generates analytics dashboard for insights
🚀 How It Works
Input video is processed frame-by-frame
YOLOv8 detects objects in each frame
DeepSORT assigns and maintains track IDs
Object trajectories are stored and visualized
Statistics are collected and plotted
📊 Output
Annotated tracking video
Object trajectories overlay
Class distribution charts
FPS performance graph
🔧 Future Improvements
Speed estimation of vehicles
Lane detection integration
Accident / anomaly detection
Real-time webcam deployment
Multi-camera tracking
