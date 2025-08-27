# Improved Diagnostic Accuracy of TMJ Osteoarthritis through Machine Learning Integration of CBCT and MRI
This repository contains the official code for the study
"Improved Diagnostic Accuracy of TMJ Osteoarthritis through Machine Learning Integration of CBCT and MRI"
by Yeon-Hee Lee, Seongwoo Jang, Seonggwang Jeon, Q–Schick Auh, and Akhilanand Chaurasia.

The repository includes data preprocessing, model training, evaluation, and visualization modules for the diagnosis of temporomandibular joint osteoarthritis (TMJ OA).

This work primarily leverages CNN-based deep learning approaches (VGG16, Fine-Tuning strategies, and Ensemble methods) applied to CBCT and MRI imaging data. The study explores how multimodal integration of imaging modalities can enhance diagnostic performance compared to single-modality approaches.

## Project Overview

Temporomandibular joint osteoarthritis (TMJ OA) is a degenerative disorder that significantly impacts oral function and patients’ quality of life.
This project investigates the diagnostic potential of CBCT and MRI imaging data using neural network models.

Key aspects include:
Preprocessing and harmonization of multimodal imaging datasets (CBCT, MRI)
CNN-based classification models (VGG16) for image-based diagnosis
Integration of patient demographic data (age, sex) with imaging features
Ensemble and fine-tuning strategies across CBCT and MRI modalities
AUROC evaluation with 95% CI and DeLong’s test for statistical comparisons

## Repository Structure

- **1_data_preprocessing.ipynb** 
  - Image resizing, normalization, patient ID matching, and label encoding  

- **2_data_initial_analyze.ipynb**
  - Dataset statistics (age, sex, OA distribution), class balance check  

- **3_Image_initial_analyze.ipynb**  
  - Visualization of representative CBCT and MRI images  
  - Basic image quality assessment (resolution, contrast)  
  - Exploratory visualization of OA vs Normal differences  

- **4_Image_Preprocessing.ipynb**
  - Image augmentation (rotation, flipping, brightness adjustment)  
  - Noise filtering and cropping for ROI (Region of Interest)  
  - Alignment of multimodal data (CBCT vs MRI consistency)  

- **5_TMJ_OA_CBCT_MRI_Training.ipynb**
  - CNN-based training with VGG16 (baseline)  
  - Fine-tuning with additional CBCT & MRI combined datasets  
  - Ensemble strategies (e.g., late fusion of CBCT and MRI models)  
  - Training/validation curve visualization, performance reporting  

- **6_Case_Delong's_test.ipynb**  
  - Statistical comparison of AUROC across models (CBCT vs MRI vs Ensemble)  
  - Pairwise DeLong’s test for significance testing  
  - Visualization of ROC curves with 95% CI  
  - Heatmap of p-values between experimental conditions  

- **README.md**  
  - Project overview, setup guide, and usage instructions
 

## Models Used

- **Neural Network Models**

  CNN (VGG16)
  Served as the baseline structure for classifying CBCT and MRI images
  Initial experiments applied VGG16 for OA vs Normal classification

- **Fine-Tuning (Transfer Learning)**

  Pretrained weights (e.g., ImageNet) applied to CBCT/MRI datasets
  Selective freezing/unfreezing of layers to optimize performance
  Conducted experiments on both single-modality (CBCT, MRI) and multimodal integration

- **Ensemble**

  Late Fusion: Combined prediction probabilities from CBCT and MRI models for final diagnosis
  Fine-tuned Ensemble: Additional fine-tuning based on integrated CBCT & MRI datasets
  Goal: Achieve higher AUROC and more stable diagnostic performance compared to single models

## Evaluation
- Performance Metrics
  AUROC (with 95% CI)
  Accuracy
  Confusion Matrix (including sensitivity and specificity)

- Statistical Comparison
  DeLong’s test performed to compare AUROC differences across models
  Pairwise comparisons:
  CBCT vs MRI
  Baseline vs New Images
  Single Modality vs Multimodal Integration (CBCT & MRI fusion)

## Contact

For any inquiries or collaboration opportunities:

- Yeon-Hee Lee: omod0209@gmail.com

- Seongwoo Jang: mook8105@cuk.edu

- Seonggwang Jeon: qq22512@hanyang.ac.kr


## Acknowledgments

- This work was supported by the Department of Orofacial Pain and Oral Medicine, Kyung Hee University Dental Hospital, and the Department of Convergence Information Studies, Korea Cyber University.
