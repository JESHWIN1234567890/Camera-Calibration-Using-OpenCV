
# 📷 Camera Calibration Using OpenCV

A Computer Vision project that calibrates a camera using a checkerboard pattern to estimate intrinsic parameters, correct lens distortion, and enable accurate real-world measurements.

This project demonstrates the complete camera calibration pipeline using **Python** and **OpenCV**, making it suitable for applications in robotics, autonomous systems, augmented reality, and computer vision.

---

## ✨ Features

- 📌 Automatic checkerboard corner detection
- 📐 Camera intrinsic matrix estimation
- 🔍 Lens distortion coefficient calculation
- 📊 Reprojection error evaluation
- 🖼️ Image undistortion
- 📏 Real-world distance measurement
- 📦 Object size estimation
- 💾 Save calibration parameters for future use

---

## 📸 Project Workflow

```text
Capture Checkerboard Images
            │
            ▼
Detect Checkerboard Corners
            │
            ▼
Generate 3D Object Points
            │
            ▼
Camera Calibration
            │
            ▼
Estimate Camera Matrix
            │
            ▼
Calculate Distortion Coefficients
            │
            ▼
Evaluate Reprojection Error
            │
            ▼
Save Calibration Parameters
            │
            ▼
Undistort Images
            │
            ▼
Distance & Size Measurement
```

---

## 🛠️ Technologies Used

- Python
- OpenCV
- NumPy
- Matplotlib

---

## 📂 Project Structure

```
Camera-Calibration-Using-OpenCV/
│
├── calibration_images/
│
├── output/
│   ├── camera_calibration.npz
│   ├── undistorted_image.jpg
│   └── comparison.png
│
├── src/
│   ├── calibrate_camera.py
│   ├── undistort_image.py
│   ├── measure_distance.py
│   └── utils.py
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## 📋 Checkerboard Configuration

| Parameter | Value |
|-----------|------:|
| Checkerboard Size | 8 × 8 Squares |
| Inner Corners | 7 × 7 |
| Square Size | 2.1 cm |
| Image Resolution | 1920 × 1080 |

---

## 📈 Calibration Results

### Camera Matrix

```text
[[1295.28      0.00    940.18]
 [   0.00   1297.94    497.08]
 [   0.00      0.00      1.00]]
```

### Distortion Coefficients

```text
k1 = 0.0625
k2 = -0.2885
p1 = ...
p2 = ...
k3 = ...
```

### Calibration Summary

| Parameter | Value |
|-----------|------:|
| Successful Images | 23 |
| RMS Error | 1.83 |
| Average Reprojection Error | 0.223 pixels |

---

## 📷 Checkerboard Used

<p align="center">
  <img src="checkerboard.jpg" width="600" alt="Checkerboard">
</p>

<p align="center">
Calibration checkerboard (8 × 8 squares with 7 × 7 inner corners) used to estimate the camera's intrinsic parameters.
</p>

---

## 🎯 Checkerboard Detection

<p align="center">
  <img src="checkerboard_detection.png" width="700" alt="Checkerboard Detection">
</p>

<p align="center">
Successful detection of checkerboard corners using OpenCV's <code>findChessboardCorners()</code> function.
</p>

---

## 🖼️ Image Undistortion

<p align="center">
  <img src="comparison.png" width="800" alt="Before vs After Undistortion">
</p>

<p align="center">
Comparison of the original distorted image and the corrected image after applying the computed camera calibration parameters.
</p>

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/Camera-Calibration-Using-OpenCV.git
```

Navigate to the project folder:

```bash
cd Camera-Calibration-Using-OpenCV
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

### Camera Calibration

```bash
python src/calibrate_camera.py
```

### Undistort Images

```bash
python src/undistort_image.py
```

### Measure Distance

```bash
python src/measure_distance.py
```

---

## 🧠 Mathematical Background

Camera calibration estimates the **intrinsic parameters** of a camera.

The intrinsic matrix is defined as:

\[
K =
\begin{bmatrix}
f_x & s & c_x\\
0 & f_y & c_y\\
0 & 0 & 1
\end{bmatrix}
\]

where:

- **fx, fy** → Focal lengths (pixels)
- **cx, cy** → Principal point
- **s** → Skew coefficient (typically zero)

The calibration process also estimates lens distortion parameters:

- Radial Distortion (k₁, k₂, k₃)
- Tangential Distortion (p₁, p₂)

These parameters are used to remove image distortion and improve measurement accuracy.

---

## 📚 Applications

- Robot Vision
- Autonomous Vehicles
- Augmented Reality (AR)
- Drone Navigation
- 3D Reconstruction
- Industrial Inspection
- Machine Vision
- Camera Pose Estimation

---

## 🔮 Future Improvements

- Real-time webcam calibration
- Stereo camera calibration
- ArUco marker calibration
- Automatic calibration image selection
- GUI application
- ROS integration
- 3D pose estimation

---

## 🤝 Contributing

Contributions are welcome.

If you have ideas for improvements or new features, feel free to open an issue or submit a pull request.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Jeshwin V S**

B.Tech Computer Science (Artificial Intelligence & Machine Learning)

Passionate about Computer Vision, Machine Learning, Deep Learning, and AI-powered applications.

---

⭐ If you found this project useful, consider giving it a star!
