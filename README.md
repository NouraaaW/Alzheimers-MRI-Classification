# Alzheimer's Disease Stage Classification Using Brain MRI Images

## Overview
This repository contains a deep learning and computer vision project aimed at automating the early detection of Alzheimer's disease using brain MRI scans. By analyzing the OASIS dataset, we evaluated multiple Convolutional Neural Network (CNN) architectures to classify MRI images into **Healthy** and **Diseased** stages.

## Key Highlights & Methodology
Rather than relying on basic models, this project implements advanced deep learning techniques to ensure clinical reliability:
* **Model Architectures:** Evaluated a Custom CNN alongside transfer learning models (VGG16 and MobileNetV2).
* **Robust Evaluation:** Utilized **patient-wise stratified 5-fold cross-validation** to prevent data leakage and ensure true generalization to unseen patients.
* **Optimization & Balancing:** Implemented **SMOTE** to handle class imbalance, combined with Grid Search hyperparameter tuning, Early Stopping, and Batch Normalization.
* **Data Augmentation:** Applied on-the-fly spatial transformations (flips, rotations, zoom) to enhance model robustness.

## Results Summary
The models were evaluated based on Accuracy, Precision, Recall, and F1-Score.
* **Custom CNN:** Achieved the highest raw accuracy (**80%**) and the strongest sensitivity for detecting diseased cases (Recall: 0.89).
* **Enhanced VGG16 (with SMOTE):** Delivered the most balanced and clinically reliable performance (**78% accuracy**) with stable generalization across both classes.
* **MobileNetV2:** Demonstrated lower performance (60%), indicating that lightweight architectures may struggle to capture the complex, distributed biomarkers of dementia.

## Repository Contents & Dataset
* `OASIS Alzheimer Dataset`: The primary dataset utilized, sourced from Kaggle. It consists of ~10,400 grayscale MRI images across 68 unique patients, organized into Healthy and Diseased classes.
* `Alzheimer's_Disease_Classification_Project.ipynb`: The complete Python notebook containing the pipeline from preprocessing and augmentation to model training and evaluation.
* `Alzheimer's Disease Classification Report.pdf`: The comprehensive report detailing dataset characteristics, methodology, and results analysis.
* `Alzheimer's Disease Classification presentation.pdf`: A visual summary of the project including confusion matrices, learning curves, and a live demo showcase.

## Tech Stack
* **Language:** Python
* **Deep Learning Framework:** TensorFlow (Keras)
* **Data Manipulation & Metrics:** Scikit-Learn, NumPy
* **Visualization:** Matplotlib, Seaborn
