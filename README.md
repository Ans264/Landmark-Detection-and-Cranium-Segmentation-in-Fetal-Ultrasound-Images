# Landmark Detection and Cranium Segmentation in Fetal Ultrasound Images

## Overview

This project consists of two main tasks:

1. **Landmark Detection-Based Approach**  
   Uses a ResNet34-based regression model to predict four biometry landmarks in fetal ultrasound images.

2. **Cranium Segmentation and Biometry Point Detection**  
   Employs a U-Net segmentation model to identify the fetal cranium, followed by post-processing to detect two biometry points.

## Usage

1. **Landmark Detection**  
   - Run `Trainer.ipynb` to train the ResNet34-based regression model.  
   - Run `Tester.ipynb` to evaluate landmark predictions and visualize the results (green circles for ground truth and red crosses for predictions).

2. **Cranium Segmentation**  
   - Run `Trainer.ipynb` to train the U-Net segmentation model.  
   - Run `Tester.ipynb` to segment the fetal cranium and detect two biometry points.

## Contents

- **Trainer.ipynb**  
  Code for training both models (regression for landmark detection, U-Net for cranium segmentation).

- **Tester.ipynb**  
  Code for model evaluation, prediction, and visualization of results.

- **Model Weights/**  
  Folder containing pre-trained weights for both models (`hypothesis_best_model_weights.pth`).

- **report.doc**  
  Detailed methodology, training procedures, experimental results, and key findings.

## Notes

- Ensure that the dataset is correctly placed in the expected directories before training.  
- The `Model Weights` folder must contain the required `.pth` file(s) for testing.  
- All paths in the notebooks are set relative to the current working directory for portability.

## Presentation

For a detailed visual explanation of the approach and results, please refer presentation file: https://www.slidespilot.com/presentations/preview/4p9Mg1z3QV
