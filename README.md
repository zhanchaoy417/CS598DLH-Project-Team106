# CS598DLH-Project-Team106

# Dataset link:

TCGA_new_pre_first.pckl https://drive.google.com/file/d/1HB7onUJkq0FbSTkrY6-HM2b1DSeU2_ox/view?usp=sharing 
TCGA_new_pre_second.pckl https://drive.google.com/file/d/1EGrv4KJiq6oZcXku8eOwQfJkmkZdiifk/view?usp=sharing

# Introduction
## Background of the Problem
The paper focuses on classifying 33 cancer tumors accurately for diagnosis and treatment. Accurate prediction of cancer types is crucial for analyzing disease causes, providing effective treatment, and understanding cancer marker genes' biological correlations. Challenges include tissue origin bias in identifying cancer markers, large databases, and complex calculations.

## Paper Explanation
Three CNN models (1D-CNN, 2D-Vanilla-CNN, 2D-Hybrid-CNN) are proposed based on different gene embedding and convolution designs. These models achieved high accuracies in cancer type prediction and identified numerous cancer markers, contributing to cancer diagnostics and marker gene biology.

# Scope of Reproducibility
## Hypotheses
1. Dataset import: Setting file paths for preprocessed data files and reading data using pd.read_pickle.
2. Build Model: Creating and training the 2D-CNN model on cancer data from The Cancer Genome Atlas (TCGA).
3. Model Training: Using k-fold cross-validation for model training.
4. Model Evaluation: Using the Adam optimizer and categorical cross-entropy loss function for model evaluation.

# Data
The pan-cancer RNA-Seq data from TCGA, comprising 10,340 samples of 33 cancer types and 713 normal tissues, were used. The raw dataset links are provided for reproducibility.

# Implementation Code
The code sets up file paths, reads preprocessed data using pd.read_pickle, builds and trains the 2D-CNN model, and evaluates its performance.

# Model
The model architecture includes Conv2D layers with specific configurations, training objectives using Adam optimizer and categorical cross-entropy loss, and preprocessing steps.

# Training
Model training involves k-fold cross-validation and input data preprocessing.

# Evaluation
The evaluation process uses metrics such as mean and standard deviation scores to assess model performance.

# Results
The CNN models achieved high prediction accuracies and identified cancer markers, enhancing cancer diagnosis. Analyses compare model performances and discuss complexities and hyperparameters.

# Plan
Reproducibility suggestions include detailed dataset documentation, code explanations, and exploring alternative data for validation.
