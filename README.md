## SALD-Net: Self-attention-integrated LiDAR-based 3D object detection network in a crowded hospital environment

SALD-Net is a self-attention-integrated LiDAR-based 3D object detection framework designed for **autonomous robot navigation** in complex environments such as hospitals. SALD-Net enhances detection accuracy for small and occluded objects through tailored attention mechanisms (BAM & RAM) and point cloud augmentation.

## Overview
- [Introduction](#introduction)
- [Network Design](#network-design)
- [Environment Settings](#environment-settings)
- [Getting Started](#getting-started)
- [Evaluation](#evaluation)

---

# Introduction
The operation of medical service robots in hospitals faces several challenges in the development of vision perception algorithms for AMRs(Autonomous Mobile Robots):

**1. Data Acquisition:**
- Problem: Risk of personal information leakage.
- Solution: Selected dataset types tailored to the unique environment.

**2. Algorithm Development:**
- Problem: Complex, crowded hospital scenes with high-risk patients (elderly or disabled).
- Solution: Enhanced contextual learning within scenes for safer operation.

**3. Data Processing:**
- Problem: Limited training data and sensor noise causing imperfect point clouds.
- Solution: Applied data augmentation and robust preprocessing pipelines.

---

# Main Ideas

Our model SALD-Net is illustrated below:

![SALD-Net Architecture](docs/images/Fig2.png)

The SALD-Net follows a two-stage end-to-end 3D detection framework: the first stage (**Initial 3D box proposal**) generates box proposals, and the second (**3D box proposal refinement**) refines them.

- The backbone extracts features via **BAM**(backbone-integrated self-attention mechanism).
- Foreground segmentation generates initial 3D box proposals, which are refined by the **URG**(unified regional and grid) RoI pooling head.
- Refined proposals are enhanced with **RAM**(RoI feature-based self-attention mechanism)

### 1. Simple Augmentation
gt autmentation

### 2. BAM
backbone

### 3. RAM
RoI pooling head 

---

# Environment Settings 
Please refer to [INSTALL.md](docs/INSTALL.md) for the installation of SALD-Net.

---

# Getting Started
Please refer to [GETTING_STARTED.md](docs/GETTING_STARTED.md) for running this project.

---

# Evaluation
Results on Custom Hospital Dataset.

| Model | BEV mAP (%) | 3D mAP (%) | Dataset | Download |
|:------|:-------------:|:-------------:|:----------|:----------|
| SALD-Net (Base) | 90.03 | 89.08 | Hospital-LiDAR | [model link](#) |

---
