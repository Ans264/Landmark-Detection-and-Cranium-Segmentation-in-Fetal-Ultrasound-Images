# Task 1: Landmark Detection-Based Approach

## Overview

This project implements a deep learning-based landmark detection model for fetal ultrasound images. The objective is to predict four biometry landmarks (two per measurement) from ultrasound data. A ResNet34-based regression model is employed to output the (x, y) coordinates for each landmark. Training is performed using the `Trainer.ipynb` notebook, and model evaluation along with visualization is done using the `Tester.ipynb` notebook. The trained model weights are saved in the `Model Weights` folder and are automatically loaded for testing. A detailed report `report.doc` is also included within the folder.

## Contents

*   `Trainer.ipynb`: Jupyter Notebook containing the code for training the segmentation model.
*   `Tester.ipynb`: Jupyter Notebook containing the code for evaluating the trained model and detecting biometry points.
*   `Model Weights/hypothesis_best_model_weights.pth`: Pre-trained weights for the segmentation model.
*   `report.doc`: A detailed report describing the methodology, results, and key findings.


## Usage

1.  **Training the Model:**

    *   Open `Trainer.ipynb` in Jupyter Notebook or JupyterLab.
    *   Run all cells in the notebook. This will train the model and save the best model weights to `Model Weights/hypothesis_best_model_weights.pth`.
    * The model is trained using a Mean Squared Error (MSE) loss, with optimization handled by the Adam optimizer and a CosineAnnealingLR scheduler ensuring smooth convergence. Early stopping is implemented to prevent overfitting.


2.  **Testing and Landmark Detection:**

    *   Open `Tester.ipynb` in Jupyter Notebook or JupyterLab.
    *   Ensure that the `hypothesis_best_model_weights.pth` file is present in the `Model Weights` directory.
    *   Run all cells in the notebook. 
    *  The Tester notebook loads the trained model and evaluates its performance by comparing predicted landmark positions against ground truth. Visual outputs overlay predicted (red crosses) and ground truth (green circles) landmarks on the test images for qualitative assessment.

## Notes

*   The paths in both `Trainer.ipynb` and `Tester.ipynb` are set to use relative paths based on the current working directory. This ensures portability across different systems.
*   The `Trainer.ipynb` notebook must be run first to generate the `hypothesis_best_model_weights.pth` file, which is required by `Tester.ipynb`.
*   The `report.doc` file provides a comprehensive overview of the project, including details on the model architecture, training procedure, and results.

## Task Description

The task focuses on predicting four biometry landmarks (two per measurement) using a regression model built on a pretrained CNN backbone - ResNet34. 