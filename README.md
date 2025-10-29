## SALD-Net: Self-attention-integrated LiDAR-based 3D object detection network in a crowded hospital environment

SALD-Net is a self-attention-integrated LiDAR-based 3D object detection framework designed for **autonomous robot navigation** in complex environments such as hospitals. SALD-Net enhances detection accuracy for small and occluded objects through tailored attention mechanisms (BAM & RAM) and point cloud augmentation.

## Overview
- [Detailed Description](#detailed-description)
- [Network Design](#network-design)
- [Environment Settings](#environment-settings)
- [Getting Started](#getting-started)
- [Evaluation](#evaluation)

---

# Detailed Description
please click to [SALD-Net.pdf link](docs/SALD-Net.pdf)

---

# Network Design

Our model SALD-Net is illustrated below:

![SALD-Net Architecture](docs/images/Fig2.png)

The SALD-Net follows a two-stage end-to-end 3D detection framework: the first stage (**Initial 3D box proposal**) generates box proposals, and the second (**3D box proposal refinement**) refines them.

- The backbone extracts features via **BAM**(backbone-integrated self-attention mechanism).
- Foreground segmentation generates initial 3D box proposals, which are refined by the **URG**(unified regional and grid) RoI pooling head.
- Refined proposals are enhanced with **RAM**(RoI feature-based self-attention mechanism)

### 1. Simple Augmentation
gt autmentation

related to code (code/)

### 2. BAM
backbone

related to code (code/)

### 3. RAM
RoI pooling head 

related to code (code/)

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
