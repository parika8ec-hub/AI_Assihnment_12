# Image Classification using Deep Learning (CIFAR-10)

## Project Overview
This project implements an image classification system using deep learning techniques on the CIFAR-10 dataset. The goal is to classify images into 10 categories such as airplane, automobile, bird, cat, deer, dog, frog, horse, ship and truck. The project compares different models including a basic neural network, an improved model with dropout and a CNN model with data augmentation to evaluate performance improvements.

---

## Dataset
- Dataset Used: CIFAR-10  
- Source: https://www.cs.toronto.edu/~kriz/cifar.html  
- Classes: 10 categories (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)  
- Image Size: 32×32 RGB images  
- Training Samples: 50,000  
- Test Samples: 10,000  

---

## Project Workflow

### 1. Data Loading
- Dataset is loaded using TensorFlow/Keras.
- Images and labels are separated into training and testing sets.

### 2. Data Visualization
- Sample images from each class are visualized to understand dataset diversity.

### 3. Data Preprocessing
- Pixel values are normalized (0–1 range).
- Labels are one-hot encoded.
- Images are flattened for Dense models.

### 4. Data Augmentation
Applied using `ImageDataGenerator`:
- Rotation
- Width shift
- Height shift
- Zoom
- Horizontal flip  

This improves model robustness by increasing training data diversity.

---

## Models Implemented

### Basic Model
- Simple feedforward neural network
- No dropout
- Used as baseline

### Improved Model
- Deeper architecture
- Dropout layers added to reduce overfitting
- Better generalization than basic model

### Augmented Model (CNN)
- Convolutional Neural Network
- Trained using augmented images
- Best performance among all models

---

## Evaluation Metrics
Models are evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Classification Report

---

## Results Summary

| Model | Accuracy | F1-score |
|------|----------|----------|
| Basic Model | ~47% | ~46% |
| Improved Model | ~40% | ~39% |
| Augmented CNN Model | ~69% | ~68% |

Data augmentation significantly improved model performance by reducing overfitting and improving generalization.

---

## How to Run the Project

### 1. Clone the Repository
git clone https://github.com/parika8ec-hub/AI_Assignment12.git

cd AI_Assignment12

### 2. Install Dependencies

pip install tensorflow numpy matplotlib seaborn scikit-learn

### 3. Open and Launch Jupyter Notebook
```bash
Open Assignment12.ipynb

Run it and execute all cells step by step
