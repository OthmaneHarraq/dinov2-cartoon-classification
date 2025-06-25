# DINOv2 Cartoon Classification

This repository contains code for evaluating the performance of the [DINOv2](https://huggingface.co/facebook/dinov2-base) Vision Transformer on a cartoon image dataset, using self-supervised features and classical classifiers.

## Description

- Extracts [CLS]-token features from cartoon images using DINOv2-base with no fine-tuning
- Handles both RGB and masked cartoon images
- Evaluates classification accuracy using:
  - Logistic Regression (best-performing classifier)
  - K-Nearest Neighbors (KNN)
- Performs classification with a 50/50 stratified train-test split
- Reports RGB, masked, and weighted total accuracy

## Results

| Classifier           | RGB Accuracy | Mask Accuracy | Weighted Accuracy |
|----------------------|--------------|----------------|--------------------|
| Logistic Regression  | 98.73%       | 89.51%         | **96.79%**         |
| K-Nearest Neighbors  | Lower        | Lower          | —                  |

> Logistic Regression consistently outperformed KNN across both image types.

## Dataset

The dataset originates from:

> **Qi Jia et al.**, “A Rotation Robust Shape Transformer for Cartoon Character Recognition,” *The Visual Computer*, 2023.

Dataset includes RGB and masked cartoon character images from 30+ classes.

Dataset link (Google Drive): [Cartoon Dataset](https://drive.google.com/drive/folders/1vhw907BYVosw7wMKmhD7CAe4x0NbenIG)

## ⚙️ Requirements

- Python ≥ 3.8  
- PyTorch  
- torchvision  
- transformers  
- scikit-learn  
- tqdm
- 
