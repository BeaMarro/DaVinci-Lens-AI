# DaVinci Lens - Painting Medium Classification System

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-CNN%20Training-orange?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red?style=for-the-badge&logo=keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-Image%20Processing-green?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Data%20Processing-blue?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Handling-darkblue?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-lightgrey?style=for-the-badge)
![Grad-CAM](https://img.shields.io/badge/Explainability-Grad--CAM-purple?style=for-the-badge)

DaVinci Lens is a computer vision system that classifies the painting medium of artworks (oil, watercolour, gouache, tempera, fresco/mural) using deep learning and a tile-based convolutional neural network approach.

This project was developed as an individual Bachelor project (Semester 7 - Enhanced AI Techniques) at Fontys University of Applied Sciences by Beatrice Marro.

It demonstrates a full end-to-end machine learning pipeline, including data engineering, model training, evaluation, explainability, and deployment via a web application.

---

## Key Performance Metrics

- Best Model: EfficientNetV2-S
- Tile-level accuracy: **~75.5%**
- <u>Full-artwork accuracy: **92.8%**</u>
- Best-performing classes: Fresco/Mural, Oil (~99%)
- Weakest class: Gouache (~80%)
- Baseline model (VGG16): validation accuracy ~70-75% with strong overfitting

Key insight:
Tile-based majority voting significantly improves real-world performance compared to individual tile classification.

---

## Project Overview

### Core Pipeline
1. Dataset ingestion (ART500K + supplementary datasets)
2. Data cleaning and filtering
3. Image tiling (150x150 optimal tile size)
4. CNN training (VGG16 → EfficientNetV2-S)
5. Model evaluation (tile-level + full-artwork inference)
6. Explainability using Grad-CAM
7. Deployment via web application (API + frontend)

---

## Model Evolution

### VGG16 Baseline
- High training accuracy (~0.95)
- Significant overfitting (validation ~0.70-0.75)
- Limited generalization

### Improved VGG16 (tuning + data improvements)
- Regularization applied
- Overfitting still present
- Inconsistent validation performance

### EfficientNetV2-S (Final Model)
- Stable convergence
- Strong generalization
- Minimal overfitting
- Best overall performance across all experiments

---

## Explainability (Grad-CAM Insights)

The model learns meaningful domain-specific visual patterns:

- Fresco/Mural: cracks, plaster texture, architectural structures
- Oil: brush strokes, blending regions, canvas texture
- Tempera: fine details and controlled stroke patterns
- Water-based media: soft gradients and paper texture

These findings confirm that the model relies on relevant artistic features rather than dataset artifacts.

---

## Web Application

A full-stack demonstration system was developed to showcase the model in a real-world scenario.

### Features
- Image upload interface
- Automatic painting medium classification
- Prediction visualization
- Backend inference API
- Frontend web interface

---

## Related Repositories

| Component | Description | Repository |
|----------|-------------|------------|
| Backend API | FastAPI inference service for model predictions | https://github.com/BeaMarro/DaVinci-Lens-API |
| Frontend Application | Web interface built using HTML, CSS, and Vanilla JavaScript | https://github.com/BeaMarro/DaVinci-Lens-Frontend |

---

## Repository Contents

This repository includes:

- Final Jupyter Notebook (.ipynb)
- Full Project Report (academic documentation)
- Presentation Slides
- Demo Video
- Trained Model Weights:
  - Final EfficientNetV2-S model
  - Experimental VGG16 and tuning variants

Some model weights are excluded due to file size constraints. They can be provided upon request.

---

## Academic Context

- Bachelor Project - Fontys University of Applied Sciences
- Semester 7 - Enhanced AI Techniques
- Individual project
- Focus areas: deep learning, computer vision, model interpretability, and applied AI system design

---

## License

This project is intended for educational and portfolio use only.

Commercial use, redistribution, or modification is not permitted without explicit written permission.

All rights reserved © 2026 Beatrice Marro

---

## Author

Beatrice Marro  
GitHub: https://github.com/BeaMarro