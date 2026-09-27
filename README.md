# Autonomous Drone GPS-Denied 6-DoF Precision Landing Estimator

![Python 3](https://img.shields.io/badge/Language-Python%203.10-blue)
![Computer Vision](https://img.shields.io/badge/Domain-Computer%20Vision%20%26%20Robotics-orange)
![Developer](https://img.shields.io/badge/Developer-Ayoub%20Lahmar-brightgreen)

A deterministic spatial computer vision pipeline for autonomous UAV precision landing in GPS-denied environments. Implements **Perspective-n-Point (PnP)** iterative solving over square fiducial targets to compute full relative \(6\text{-DoF}\) transformation matrices (\(t_x, t_y, t_z, \theta_{\text{yaw}}, \theta_{\text{pitch}}, \theta_{\text{roll}}\)).

Implemented by **Ayoub Lahmar** ([@Redayoub-lang](https://github.com/Redayoub-lang)).

## 📐 Spatial Transformation Model

World frame target coordinates \(P_w\) transform to optical camera coordinates \(P_c\) via:

$$
P_c = R \cdot P_w + T
$$

Where \(R \in \mathrm{SO}(3)\) is computed via Rodrigues transform over rotation vector \(r_{\text{vec}}\), and \(T \in \mathbb{R}^3\) specifies Cartesian spatial translation vector \((t_x, t_y, t_z)^T\).

## 💻 Build & Run

```bash
pip install opencv-python numpy
python landing_estimator.py
