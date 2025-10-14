 JuaShade: A Computer Vision Pipeline for Skin Tone Analysis and Color Constancy

⸻

🧠 Overview

JuaShade is a computer vision research project that focuses on fair and accurate skin tone analysis.
Many computer vision systems misinterpret skin tones because of lighting variations, glare, and dataset bias, resulting in inaccurate or non-inclusive outcomes.

This project proposes a modular computer vision pipeline that:
	•	Extracts skin regions of interest (ROI)
	•	Removes glare and reflections
	•	Applies color constancy algorithms such as Gray-World and Retinex
	•	Compares classical ML models (SVM, k-NN) with deep learning architectures (ResNet, EfficientNet)
	•	Incorporates GAN-based preprocessing to improve tone normalization

The goal is to create a fair, inclusive, and robust system applicable in dermatology, cosmetics, and AI fairness research