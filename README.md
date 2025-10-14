🧩 Project Title

JuaShade: A Computer Vision Pipeline for Skin Tone Analysis and Color Constancy

🧠 Overview

JuaShade is a computer vision research project focused on improving fair and accurate skin tone analysis.
Many computer vision systems misinterpret skin tones because of lighting variations, glare, and dataset bias, which can lead to inaccurate or non-inclusive results.

This project introduces a modular pipeline that:
	•	Extracts skin regions of interest (ROI)
	•	Removes glare and reflections
	•	Applies color constancy algorithms (Gray-World, Retinex)
	•	Compares classical ML models (SVM, k-NN) with deep learning architectures (ResNet, EfficientNet)
	•	Explores GAN-based preprocessing to improve tone normalization

The goal is to develop a fair, inclusive, and robust system for use in dermatology, cosmetics, and AI fairness research.

⸻

⚙️ Tech Stack
	•	Languages: Python
	•	Libraries: OpenCV, scikit-image, scikit-learn, NumPy, PyTorch
	•	Tools: Jupyter Notebook, Matplotlib

Input Image
   ↓
Skin ROI Extraction
   ↓
Glare / Reflection Removal
   ↓
Color Constancy Correction
   ↓
Feature Extraction (ML/DL)
   ↓
Tone Classification + Fairness Evaluation
