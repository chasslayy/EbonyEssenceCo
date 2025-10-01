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

## Future Extensions
While LumiSkin is currently a research prototype, the framework can be extended into real-world applications for both customers and businesses:

- **AR Shade Try-On** → Integrate the skin swatch extraction pipeline into augmented reality apps for live foundation and makeup shade testing.  
- **E-Commerce Integration** → Provide APIs that beauty brands can embed into their online stores to offer personalized shade recommendations.  
- **Virtual Consultations** → Power digital skincare and beauty consultations, giving users true-to-life skin analysis directly from selfies.  
- **Hair & Makeup Expansion** → Extend the pipeline to handle hair segmentation, makeup transfer, or complete face analysis for end-to-end beauty personalization.  
- **Dermatology Applications** → Adapt LumiSkin for skin health monitoring, enabling consistent color analysis for medical or skincare diagnostics.  
- **Dataset Contributions** → Curate an open dataset of lighting-varied skin images to advance fairness and inclusivity in beauty AI.  
