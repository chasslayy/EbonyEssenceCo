# 🌞 JuaShade: A Computer Vision Pipeline for Skin Tone Analysis & Color Constancy

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red.svg)](https://pytorch.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg)](https://opencv.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **Goal:** Fair, robust skin-tone analysis across lighting conditions by combining ROI extraction, glare removal, color constancy, and both classical & deep models—plus optional GAN preprocessing.

---

## 🧠 Overview
Traditional vision systems often misread skin tones due to **lighting variation, glare, and dataset bias**.  
**JuaShade** introduces a **modular pipeline** to:
- Extract **skin ROIs**
- Remove **glare/reflections**
- Apply **color constancy** (Gray-World, Retinex)
- Compare **SVM/k-NN** vs **ResNet/EfficientNet**
- (Optional) Use **GANs** for tone enhancement
- Report **fairness & color consistency** metrics

---

## 🧱 Pipeline (High-Level)

python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows (PowerShell)
.venv\Scripts\Activate.ps1

pip install --upgrade pip
pip install -r requirements.txt

python scripts/preprocess.py \
  --in_dir data/raw \
  --out_dir data/processed \
  --roi_method ycrcb \
  --glare remove \
  --color_constancy retinex

python scripts/train_classical.py \
  --data_dir data/processed \
  --features hog \
  --models svm knn \
  --out_dir results/classical

python scripts/evaluate.py \
  --pred_dirs results/classical results/deep \
  --metric_groups accuracy deltaE fairness \
  --out_dir results/metrics

python scripts/gan_enhance.py \
  --in_dir data/raw \
  --out_dir data/gan_enhanced \
  --gan pix2pix

jupyter notebook notebooks/00_quick_demo.ipynb

JuaShade/
├─ data/
│  ├─ raw/              # raw images (not committed)
│  └─ processed/        # preprocessed outputs
├─ notebooks/
│  ├─ 00_quick_demo.ipynb
│  ├─ 10_preprocess_examples.ipynb
│  └─ 20_model_eval.ipynb
├─ src/
│  ├─ preprocessing/
│  │  ├─ roi.py
│  │  ├─ glare.py
│  │  └─ color_constancy.py
│  ├─ models/
│  │  ├─ classical.py
│  │  ├─ resnet.py
│  │  └─ efficientnet.py
│  └─ evaluation/
│     ├─ metrics.py
│     └─ fairness.py
├─ scripts/
│  ├─ prepare_data.py
│  ├─ preprocess.py
│  ├─ train_classical.py
│  ├─ train_deep.py
│  ├─ gan_enhance.py
│  └─ evaluate.py
├─ results/
│  ├─ classical/
│  ├─ deep/
│  └─ metrics/
├─ requirements.txt
└─ README.md