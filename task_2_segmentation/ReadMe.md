# Task 2: Fetal Cranium Segmentation and Biometry Point Detection

## Overview

This project implements a deep learning-based approach for segmenting the fetal cranium in ultrasound images and subsequently detecting key biometry points using computer vision techniques. The workflow involves training a segmentation model (U-Net) to identify the cranium, followed by a post-processing step to locate two biometry points of interest.

## Contents

*   `Trainer.ipynb`: Jupyter Notebook containing the code for training the segmentation model.
*   `Tester.ipynb`: Jupyter Notebook containing the code for evaluating the trained model and detecting biometry points.
*   `Model Weights/hypothesis_best_model_weights.pth`: Pre-trained weights for the segmentation model.
*   `report.doc`: A detailed report describing the methodology, results, and key findings.


## Usage

1.  **Training the Segmentation Model:**

    *   Open `Trainer.ipynb` in Jupyter Notebook or JupyterLab.
    *   Run all cells in the notebook. This will train the U-Net model and save the best model weights to `Model Weights/hypothesis_best_model_weights.pth`.

2.  **Testing and Biometry Point Detection:**

    *   Open `Tester.ipynb` in Jupyter Notebook or JupyterLab.
    *   Ensure that the `hypothesis_best_model_weights.pth` file is present in the `Model Weights` directory.
    *   Run all cells in the notebook. This will load the trained model, perform segmentation on test images, and detect the biometry points using computer vision algorithms.

## Notes

*   The paths in both `Trainer.ipynb` and `Tester.ipynb` are set to use relative paths based on the current working directory. This ensures portability across different systems.
*   The `Trainer.ipynb` notebook must be run first to generate the `hypothesis_best_model_weights.pth` file, which is required by `Tester.ipynb`.
*   The `report.doc` file provides a comprehensive overview of the project, including details on the model architecture, training procedure, and results.

## Task Description

The task involves training a segmentation model to identify the cranium in ultrasound images. The dataset includes ellipse-fit annotations for the cranium, which are used to guide the training process. After training, a computer vision algorithm is used to find two biometry points on the segmented cranium.