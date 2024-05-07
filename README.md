# CS598DLH-Project-Team106

- Class: CS598 Deep Learning for Healthcare, Spring 2024

- **Project Team #106:**

  *   Zhanchao Yang: zy45@illinois.edu
  *   Bin Li: binl3@illinois.edu
  *   Yutang Lin: yutangl2@illinois.edu
  *   
# Video link:

# Dataset link:
1. TCGA_new_pre_first.pckl https://drive.google.com/file/d/1HB7onUJkq0FbSTkrY6-HM2b1DSeU2_ox/view?usp=sharing 

2. TCGA_new_pre_second.pckl https://drive.google.com/file/d/1EGrv4KJiq6oZcXku8eOwQfJkmkZdiifk/view?usp=sharing

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
## Data descriptions
The pan-cancer RNA-Seq data from TCGA, comprising 10,340 samples of 33 cancer types and 713 normal tissues, were used. The raw dataset links are provided for reproducibility.

# Implementation Code
The code sets up file paths, reads preprocessed data using pd.read_pickle, builds and trains the 2D-CNN model, and evaluates its performance.

# Model
## Model descriptions
The model architecture includes Conv2D layers with specific configurations, training objectives using Adam optimizer and categorical cross-entropy loss, and preprocessing steps.

# Training
## Hyperparameters Report
- learning_rate = 0.01
- batch_size = 32
- hidden_size = 128
- dropout_rate = 0.2

## Computational Requirements Report
- Hardware Type:NVIDIA GeForce GTX GPU, Intel i5-8400, 16 GB memory
- Average Runtime per Epoch: 1~2 minutes
- Total number of trials: 5 trials per fold for 10-fold cross-validation, hence 50 trials in total
- GPU Hours Used:Estimated GPU hours used for training for each teammate: 20, 25, 25 hours. Hence Average GPU hours used for training: 23.33 hours
  
# Evaluation
## Evaluation descriptions
During the elution process, we used the Adam optimizer and the categorical cross-entropy loss function. The Adam optimizer can quickly and efficiently converge to obtain results in large and complex data sets, while the Categorical Cross-Entropy loss function is used to measure the difference between the predicted cancer category probability and the true label

# Results
Our Results achieved excellent average accuracies 95% among 34 classes (33 cancers and normal). Furthermore, we interpreted the 1D-CNN， Vanilla-CNN, and Hybrid-CNN model with a guided saliency technique and identified a total of 2,090 cancer markers (108 per class).

# Discussion
Reproducibility suggestions include detailed dataset documentation, code explanations, and exploring alternative data for validation.

# References
1.  Mostavi, M., Chiu, YC., Huang, Y. et al. Convolutional neural network models for cancer type prediction based on gene expression. BMC Med Genomics 13 (Suppl 5), 44 (2020). https://doi.org/10.1186/s12920-020-0677-2

