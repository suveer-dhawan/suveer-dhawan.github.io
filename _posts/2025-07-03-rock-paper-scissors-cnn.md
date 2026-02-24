---
title: "Computer Vision: 99.7% Accuracy with Custom PyTorch CNNs"
date: 2025-07-03 12:00:00 +0530
categories: [Projects, Deep Learning]
tags: [pytorch, cnn, computer-vision, model-evaluation]
pin: true
---

**Role:** Monash Deep Neuron Team Project  
**Location:** Melbourne, Australia  
**Timeline:** May 2025 – July 2025  

While pre-trained models are powerful, I wanted to build and optimize a Convolutional Neural Network (CNN) entirely from scratch. For this project, I architected a deep learning model to classify hand gestures (Rock, Paper, Scissors), progressing from a simple baseline to a robust, highly optimized architecture.

### Architecture & Training Strategy

I built the models utilizing **PyTorch**, executing the training loops on Google Colab Pro for GPU acceleration. 

* **The "DeeperCNN" Architecture:** I designed a custom sequential model integrating Batch Normalization (`nn.BatchNorm2d`) and Dropout layers (`nn.Dropout2d`) to handle intricate image patterns and prevent overfitting.
* **Advanced Training Techniques:** I implemented a dynamic Learning Rate Scheduler (`ReduceLROnPlateau`) to fine-tune weights as the model approached optimal performance, alongside a custom Early Stopping class that automatically restored the best-performing weights.
* **Data Augmentation:** Engineered a robust transformation pipeline (RandomAffine, ColorJitter, GaussianBlur) to ensure the model could generalize across different lighting conditions and hand orientations.

### Performance & Rigorous Testing

The optimized model achieved a near-perfect **99.73% accuracy** on a completely unseen test dataset. 

However, high accuracy isn't enough; a model must be well-calibrated. I conducted comprehensive evaluation tests beyond basic metrics:
* **Confidence Distribution Analysis:** Proved that the model exhibits high confidence (near 100%) on correct predictions, and crucially, lower confidence on misclassifications.
* **Class Confusion Matrix:** Demonstrated an almost perfectly diagonal matrix, visually confirming the model's reliability across all three classes without systemic bias.

This project solidified my foundational understanding of deep learning mechanics—from custom DataLoader pipelines to hyperparameter tuning and reproducible experiment tracking.