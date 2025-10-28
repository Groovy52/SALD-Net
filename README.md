# SALD-Net: Self-Attention LiDAR Detection Network

## 📑 Table of Contents
- [Changelog](#changelog)
- [Design Pattern](#design-pattern)
- [Model Zoo](#model-zoo)
- [Installation](#installation)
- [Quick Demo](#quick-demo)
- [Getting Started](#getting-started)
- [Citation](#citation)

---

## 🧩 Changelog

- **[2025.10.28]** Initial version of SALD-Net uploaded.
- **[2025.11.xx]** Add demo video and pretrained model links.

---

## 🧠 Design Pattern

- Backbone: Point-based feature extraction  
- Head: Unified Regional & Grid (URG) RoI pooling  
- Self-Attention modules: BAM / RAM  
- Framework overview diagram (추가 예정)

---

## 🧰 Model Zoo

| Model | BEV mAP (%) | 3D mAP (%) | Dataset | Download |
|:------|:-------------:|:-------------:|:----------|:----------|
| SALD-Net (Base) | 90.03 | 89.08 | Hospital-LiDAR | [model link](#) |

---

## ⚙️ Installation

```bash
# 1. 환경 설정
conda create -n saldnet python=3.8
conda activate saldnet

# 2. 필수 패키지 설치
pip install -r requirements.txt

# 3. CUDA 환경 테스트
python demo/test_cuda.py
