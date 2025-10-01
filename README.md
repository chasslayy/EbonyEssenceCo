# LumiSkin: Photo-Robust Skin Swatch Extraction with Computer Vision

## Overview
**LumiSkin** is a computer vision project that focuses on extracting reliable skin color swatches from facial images under varied lighting conditions. Accurate skin color estimation is essential in beauty technology applications such as foundation shade matching, virtual try-on, and personalized skincare.  

Selfies and consumer photos are often distorted by glare, shadows, and inconsistent lighting, making skin tone analysis unreliable. LumiSkin proposes a robust pipeline that isolates stable regions of interest (cheek and forehead), applies glare removal and color constancy methods, and converts results into perceptually uniform color spaces (CIELAB) for consistent skin swatch extraction.

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
