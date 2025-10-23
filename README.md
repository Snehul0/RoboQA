<p align="center">
  <img src="RoboQA%20Logo%2020251023.png" alt="RoboQA Logo" width="220"/>
</p>

<h1 align="center">RoboQA</h1>
<p align="center">
  An open-source ROS2 framework for data quality assurance in autonomous driving datasets.
</p>

---

## 🚗 Overview

**RoboQA** is a ROS2-based framework that automatically detects temporal desynchronization and data anomalies across multimodal autonomous-driving datasets (LiDAR, camera, radar, IMU, etc.).  
It provides a quality-assurance layer between data collection and model training—catching synchronization errors and sensor degradation before expensive labeling or GPU training begins.

---

## 🧠 Key Features
- ⏱️ **Temporal Alignment Check** – Detects desynchronization between LiDAR, camera, radar, and IMU streams.  
- 🔍 **Data Anomaly Detection** – Flags missing frames, corrupted files, or degraded sensor readings.  
- 🧩 **ROS2 Integration** – Seamlessly plugs into your existing ROS2 pipelines.  
- 📊 **Visual Reports** – Summarizes data integrity and synchronization status.  
- 🧱 **Extensible Design** – Easy to adapt for new sensors or custom validation rules.  

---

## 🛠️ Installation

```bash
# Clone the repo
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

# Build using colcon (ROS2)
colcon build
source install/setup.bash

Autonomous driving systems rely on large multimodal datasets combining LiDAR, camera, radar, and IMU sensors. These datasets fuel perception and sensor-fusion models, yet the quality of raw sensor data is rarely verified before training. In practice, many teams discover too late that model underperformance stems not from architecture choices but from poor data synchronization or sensor degradation.
Current tools such as Open3D or PCL allow engineers to view or filter point clouds but do not evaluate whether LiDAR and camera streams are temporally aligned. Similarly, ROS testing frameworks like HAROS focus on software nodes rather than data content. This lack of systematic data validation results in wasted GPU hours, inconsistent benchmarks, and unreliable reproducibility.
This project proposes RoboQA-Temporal, an open-source ROS2 framework that automatically detects temporal desynchronization and data anomalies in autonomous-driving datasets. The goal is to create a quality-assurance layer between data collection and model training—catching errors before expensive labeling or learning begins.
