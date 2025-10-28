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

1. 데이터 획득 과정에서 문제-개인정보 유출
2. 알고리즘 개발 과정에서 문제: 복잡, 혼잡, 중앙보훈병원의 경우 충돌 시 생명에 큰 위협이 되는 고령, 장애를 가진 환자 입원
3. 학습 데이터 획득, 처리 과정에서 문제: 일반화 학습 데이터셋 자체량 부족, 센서 노이즈 등 포인트 클라우드 자체 결함 존재 -> 전처리 프로세스 필수


---

# Network Design
Our model SALD-Net is illustrated below:

![SALD-Net Architecture](docs/images/Fig2.png)

The SALD-Net follows a two-stage end-to-end 3D detection framework: the first stage (**Initial 3D box proposal**) generates box proposals, and the second (**3D box proposal refinement**) refines them.

- The backbone extracts features via **BAM**(backbone-integrated self-attention mechanism).
- Foreground segmentation generates initial 3D box proposals, which are refined by the **URG**(unified regional and grid) RoI pooling head.
- Refined proposals are enhanced with **RAM**(RoI feature-based self-attention mechanism)

## Training Pipeline
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
