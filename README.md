# LumiSkin: Photo-Robust Skin Swatch Extraction with Computer Vision

## Overview

LumiSkin is designed as more than a research project — it’s a prototype for the next generation of beauty-tech.  

- **True-to-Life Skin Tones** → Reduce distortions from lighting, glare, and shadows so selfies reflect real skin tones.  
- **Inclusive by Design** → Support accurate shade analysis across the full spectrum of skin tones, ensuring equity in foundation and skincare matching.  
- **Beauty x Tech Innovation** → Provide a computer vision pipeline that beauty brands can integrate into AR try-on apps, virtual consultations, or shade finder tools.  
- **Reliable Color Data** → Generate stable, repeatable CIELAB swatches that serve as trusted inputs for AI shade recommendation systems.  
- **Empowering Customers & Brands** → Help individuals choose products with confidence, while enabling businesses like L’Oréal or Sephora to improve personalization.  

---

## Objectives
- Detect faces and extract cheek/forehead regions using landmark detection.  
- Reduce distortions by removing glare and highlights.  
- Apply color constancy algorithms (Gray-World, Shades-of-Gray, Retinex).  
- Convert corrected skin regions into CIELAB space.  
- Extract and visualize stable skin swatches across lighting conditions.  
- Quantitatively evaluate results with ΔE (color difference) and ablation studies.  

---

## Methods
- **Landmark Detection:** MediaPipe Face Mesh / dlib  
- **ROI Extraction:** Cheek and forehead skin patches  
- **Glare Removal:** HSV thresholding + inpainting  
- **Color Constancy:** Gray-World, Shades-of-Gray, Retinex  
- **Color Space Conversion:** RGB → CIELAB for perceptual accuracy  
- **Evaluation:**  
  - ΔE variance across lighting setups  
  - Ablations (glare removal on/off, algorithm comparisons, ROI choice)  
  - User study for realism/consistency ratings  

---

## Repo Structure
