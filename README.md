# Improved Diagnostic Accuracy of TMJ Osteoarthritis through Machine Learning Integration of CBCT and MRI
This repository contains the official code for the study
"Improved Diagnostic Accuracy of TMJ Osteoarthritis through Machine Learning Integration of CBCT and MRI"
by Yeon-Hee Lee, Seongwoo Jang, Seonggwang Jeon, Q–Schick Auh, and Akhilanand Chaurasia.

The repository includes data preprocessing, model training, evaluation, and visualization modules for the diagnosis of temporomandibular joint osteoarthritis (TMJ OA).

This work primarily leverages CNN-based deep learning approaches (VGG16, Fine-Tuning strategies, and Ensemble methods) applied to CBCT and MRI imaging data. The study explores how multimodal integration of imaging modalities can enhance diagnostic performance compared to single-modality approaches.

#Project Overview

Temporomandibular joint osteoarthritis (TMJ OA) is a degenerative disorder that significantly impacts oral function and patients’ quality of life.
This project investigates the diagnostic potential of CBCT and MRI imaging data using neural network models.

Key aspects include:

Preprocessing and harmonization of multimodal imaging datasets (CBCT, MRI)

CNN-based classification models (VGG16) for image-based diagnosis

Integration of patient demographic data (age, sex) with imaging features

Ensemble and fine-tuning strategies across CBCT and MRI modalities

AUROC evaluation with 95% CI and DeLong’s test for statistical comparisons
