🧠 Overview

JuaShade is a computer vision research project that improves fair and accurate skin tone analysis.
Traditional vision systems often misinterpret skin tones due to lighting variation, glare, and dataset bias, which can lead to inaccurate or biased outcomes.

This project creates a modular pipeline that:
	•	Extracts skin regions of interest (ROI)
	•	Removes glare and reflections
	•	Applies color constancy (Gray-World, Retinex)
	•	Compares SVM/k-NN vs. ResNet/EfficientNet
	•	Explores GAN-based tone enhancement

The goal is to build a fair, inclusive, and robust AI model for use in dermatology, beauty tech, and fairness research.

⚙️ Tech Stack
	•	Languages: Python
	•	Libraries: OpenCV, scikit-image, scikit-learn, NumPy, PyTorch
	•	Tools: Jupyter Notebook, Matplotlib