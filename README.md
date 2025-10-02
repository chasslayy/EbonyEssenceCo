# Ebony Essence Co: Photo-Robust Skin Swatch Extraction with Computer Vision  

## Overview  
**Ebony Essence Co ** is a computer vision project that focuses on extracting reliable skin color swatches from facial images under varied lighting conditions. Accurate skin color estimation is a key challenge in beauty technology, powering applications such as foundation shade matching, AR try-on, personalized skincare, and even dermatology analysis.  

Selfies are often distorted by glare, shadows, and inconsistent lighting, which makes skin tone analysis unreliable. LumiSkin introduces a pipeline that detects stable facial regions, removes glare, applies color constancy algorithms, and generates consistent skin tone swatches in the CIELAB color space.  

This project bridges **AI, beauty, and innovation** — providing not only a research prototype for computer vision coursework but also a foundation for future real-world applications in the beauty-tech industry.  

---

## Objectives  
- **True-to-Life Skin Tones** → Minimize lighting distortions so selfies reflect authentic skin color.  
- **Inclusive by Design** → Deliver consistent analysis across all skin tones, supporting equitable shade matching.  
- **Beauty x Tech Innovation** → Provide a pipeline that can integrate into AR apps, e-commerce platforms, and virtual consultations.  
- **Reliable Color Data** → Generate stable CIELAB swatches that serve as inputs for machine learning shade recommendation systems.  
- **Empowering Customers & Brands** → Help individuals shop confidently while enabling beauty companies to personalize product experiences.  

---

## Methods  
- **Landmark Detection:** MediaPipe Face Mesh / dlib for facial ROI extraction (cheek & forehead).  
- **Glare Removal:** HSV thresholding and inpainting to reduce highlight distortions.  
- **Color Constancy:** Gray-World, Shades-of-Gray, and Retinex methods for lighting normalization.  
- **Color Conversion:** RGB → CIELAB for perceptual accuracy.  
- **Evaluation:**  
  - *Color Stability KPI* → ΔE variance across lighting conditions.  
  - *Mask Precision* → ROI accuracy vs ground truth.  
  - *Ablations* → With/without glare removal, different constancy methods, ROI choices.  
  - *User Study* → Ratings of realism and consistency.  

---

## Repo Structure  

