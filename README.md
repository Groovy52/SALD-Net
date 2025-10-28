## SALD-Net: Self-attention-integrated LiDAR-based 3D object detection network in a crowded hospital environment

SALD-Net is a self-attention-integrated LiDAR-based 3D object detection framework designed for **autonomous robot navigation** in complex environments such as hospitals. SALD-Net enhances detection accuracy for small and occluded objects through tailored attention mechanisms (BAM & RAM) and point cloud augmentation.

## Table of Contents
- [Network](#network)
- [Environment Settings](#environment-settings)
- [Getting Started](#getting-started)
- [Evaluation](#evaluation)

---

# Network 
Our model SALD-Net is illustrated below:
(.png)

## Training Pipeline
### 1. Simple Augmentation
gt autmentation

### 2. BAM
backbone

### 3. RAM
RoI pooling head 

---

# Environment Settings 
Please refer to INSTALL.md for the installation of SALD-Net.

---

# Getting Started
Please refer to GETTING_STARTED.md for running this project.

---

# Evaluation
Results on Custom Hospital Dataset.

| Model | BEV mAP (%) | 3D mAP (%) | Dataset | Download |
|:------|:-------------:|:-------------:|:----------|:----------|
| SALD-Net (Base) | 90.03 | 89.08 | Hospital-LiDAR | [model link](#) |

---
