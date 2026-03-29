# 🌪️ Cyclone Detection using Deep Learning

## 📌 Overview

This project focuses on detecting and analyzing cyclones using satellite imagery and deep learning techniques. By leveraging temporal patterns in meteorological data, the system distinguishes between cyclone and non-cyclone events.

The workflow integrates data preprocessing, visualization, temporal feature extraction, and deep learning-based classification.

---

## 🛰️ Dataset

* Source: Satellite data in **NetCDF (.nc)** format
* Variable used: **CMI (Cloud and Moisture Imagery)**
* Data includes:

  * Spatial dimensions (latitude, longitude)
  * Temporal sequences (time-series frames)

---

## ⚙️ Data Preprocessing

### 1. Spatial Cropping

To focus on relevant regions:

* Selected geographical bounding box
* Reduced unnecessary spatial noise

### 2. Resolution Reduction

* Applied spatial coarsening to improve performance
* Downsampled frames for faster processing

### 3. Temporal Sampling

* Skipped frames to reduce redundancy
* Maintained essential temporal patterns

---

## 📊 Feature Engineering

### 🌡️ Cyclone Intensity Estimation

* Extracted **minimum brightness temperature** per frame
* Based on the principle:

  > Lower cloud-top temperatures indicate stronger convection and cyclone activity

### 📉 Temporal Smoothing

* Applied rolling average to remove noise
* Improved trend visualization of cyclone intensity

---

## 🧠 Model Architecture

The model leverages temporal dependencies in satellite imagery using deep learning.

* Input: Sequence of satellite frames
* Core layers:

  * ConvLSTM / LSTM layers for temporal learning
  * Batch normalization for stability
  * Dense layer for classification

---

## 📈 Visualization

The project includes:

* Frame-wise satellite image visualization
* Cyclone evolution animations
* Intensity trend graphs over time

---

## ▶️ Usage

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run the project

```bash
python train.py
```

---

## 📁 Project Structure

```
cyclone-detection-deep-learning/
│
├── notebooks/        # Jupyter experiments
├── src/              # Core logic (model, preprocessing)
├── models/           # Saved models
├── results/          # Outputs and plots
│
├── README.md
├── requirements.txt
└── train.py
```

---

## 🚀 Future Improvements

* Transformer-based temporal models
* Real-time cyclone tracking
* Multi-channel satellite data integration
* Deployment as a web application

---

## 🤝 Contribution

Contributions, issues, and suggestions are welcome!

---

## 📜 License

This project is licensed under the MIT License.
