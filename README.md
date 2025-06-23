# DINOv2 Cartoon Classification

This repository contains code for evaluating the performance of the [DINOv2](https://huggingface.co/facebook/dinov2-base) Vision Transformer on a cartoon image dataset, using self-supervised features and classical classifiers.

## 📚 Description

- Extracts CLS-token features from cartoon images using DINOv2
- Handles both RGB and masked cartoon images
- Evaluates classification accuracy using:
  - Logistic Regression
  - K-Nearest Neighbors (KNN)

The dataset used in this project originates from the paper:

> *Qi Jia et al., “A Rotation Robust Shape Transformer for Cartoon Character Recognition,” The Visual Computer, 2023.*

## 📁 Dataset

Available [here](https://drive.google.com/drive/folders/1vhw907BYVosw7wMKmhD7CAe4x0NbenIG) (Google Drive link provided by the authors).

## 🛠️ Requirements

- Python ≥ 3.8  
- PyTorch  
- torchvision  
- transformers  
- scikit-learn  
- tqdm

Install dependencies with:
```bash
pip install torch torchvision transformers scikit-learn tqdm
