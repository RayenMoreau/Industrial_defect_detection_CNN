# Industrial Surface Defect Detection using Deep Learning

##  Project Overview
This project focuses on automatic detection and classification of industrial surface defects using deep learning.  
A convolutional neural network is trained to classify images of steel surfaces into different defect categories, helping reduce reliance on manual inspection.

##  Problem Statement
Manual visual inspection in industrial manufacturing is:
- time-consuming
- expensive
- prone to human error

This project demonstrates how a CNN can automatically detect and classify surface defects with high accuracy while also providing visual explanations of its decisions.

##  Dataset
- **NEU Surface Defect Database (NEU-CLS)**
- 6 defect classes:
  - Crazing
  - Inclusion
  - Patches
  - Pitted Surface
  - Rolled-in Scale
  - Scratches
- Grayscale images
- Dataset split:
  - Train: 70%
  - Validation: 15%
  - Test: 15%

##  Model
- Backbone: **MobileNetV2 (ImageNet pretrained)**
- Transfer learning with frozen base model
- Custom classification head
- Data augmentation applied during training

##  Training Details
- Optimizer: Adam
- Loss: Categorical Cross-Entropy
- Early stopping to prevent overfitting
- Final Test Accuracy: **98.33%**

##  Evaluation
Model performance was evaluated using:
- Confusion Matrix
- Precision / Recall / F1-score
- ROC curves (one-vs-rest)

These metrics help analyze class-level performance and misclassifications.

##  Explainability (Grad-CAM)
Grad-CAM was applied to visualize which regions of an image influenced the model’s predictions.  
This confirms that the network focuses on actual defect regions rather than background textures.

Example outputs include:
- Correct predictions
- Misclassified samples with visual explanations

##  Tools & Technologies
- Python
- TensorFlow / Keras
- scikit-learn
- OpenCV
- Google Colab

##  Optional Extensions
- TensorFlow Lite conversion for edge deployment
- Raspberry Pi inference
- Defect localization (segmentation)

##  Conclusion
This project demonstrates a complete industrial computer vision pipeline:
from data preparation and training to evaluation and explainable AI.

