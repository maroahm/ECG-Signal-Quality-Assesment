# ECG Signal Quality Assessment using a Multi-Scale VPNet-LSTM

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange)
![License](https://img.shields.io/badge/License-MIT-green)

This repository contains the complete code and findings for a research project on assessing electrocardiogram (ECG) signal quality. The project implements a novel deep learning architecture, the Multi-Scale VPNet-LSTM, which proved highly effective for this classification task.

## Project Overview

The reliability of ECG data is crucial for clinical diagnosis and wearable health monitoring. This project tackles the challenge of automatically classifying the quality of individual heartbeats into three categories: **Good**, **Intermediate**, and **Bad**.

The core innovation of this project is a **multi-scale architecture** that addresses the failure of a standard, single-scale baseline model. By using a "team of experts"—three parallel Variable Projection Network (VPNet) branches each tuned to a different feature scale—the model creates a rich, comprehensive representation of the ECG signal's morphology. This approach led to a high-performing final model that significantly outperformed previous baselines.

### Key Achievements
- **Architected a novel multi-scale VPNet-LSTM model** in PyTorch, achieving a final **F1-score of 84.65%** on the challenging 3-class problem.
- **Developed a systematic diagnostic pipeline** with custom visualization scripts (Matplotlib) to identify and resolve a critical failure in the initial non-learning baseline model.
- **Engineered a parallel "team of experts" feature extractor** that captures both wide, slow-wave features and sharp, high-frequency spikes in the ECG signal.
- **Managed the end-to-end research cycle**, from diagnosing the initial problem to proposing, implementing, and validating a superior architectural solution.

## Final Results

The final, optimized model was trained for 80 epochs and evaluated on an unseen test set.

#### Performance Metrics
| Metric | Score |
| :--- | :--- |
| **F1-Score (Weighted)** | **84.65%** |
| Accuracy | 82.62% |
| Precision (Weighted) | 89.15% |
| Recall (Weighted) | 82.62% |

#### Confusion Matrix
The confusion matrix highlights the model's behavior, showing particular strength in identifying "Bad" quality signals, which is critical for data filtering applications.

![Confusion Matrix for Best Model](path/to/your/confusion_matrix.png)

*You should save the `confusion_matrix.png` file you generated into a folder like `images/` and update the path above.*

## Model Architecture

The final model uses a multi-stage process to classify the ECG signals. The key innovation is the parallel feature extraction stage.

![Multi-Scale Architecture Diagram](path/to/your/architecture_diagram.png)

*You should create the simple diagram we discussed, save it as an image, and update the path above.*

## Technology Stack
- **Language:** Python
- **Core Libraries:** PyTorch, Pandas, NumPy, Scikit-learn
- **Visualization:** Matplotlib, Seaborn

## Setup and Installation

To run this project, it is recommended to use a virtual environment.

**1. Clone the repository:**
```bash
git clone https://github.com/maroahm/ECG-Signal-Quality-Assesment
