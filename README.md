# CIFAR-10_CNN_Image-Classification
# CIFAR-10 CNN Image Classification

A Convolutional Neural Network (CNN) based image classification project developed as part of the EncoderX AI/ML Internship.

The model is trained on the **CIFAR-10 dataset** to classify images into 10 different categories.

## 📌 Project Overview

This project demonstrates an end-to-end image classification workflow using **TensorFlow/Keras**, starting from dataset understanding and preprocessing to CNN model development, training, evaluation, and error analysis.

### CIFAR-10 Classes

The model classifies images into the following 10 categories:

* Airplane
* Automobile
* Bird
* Cat
* Deer
* Dog
* Frog
* Horse
* Ship
* Truck

## 🔄 Project Workflow

### Phase 1 — Data

* Dataset selection
* Dataset understanding
* Exploratory Data Analysis (EDA)
* Image and label verification
* Train/validation/test split
* Pixel normalization
* Data augmentation

### Phase 2 — Model

* CNN architecture design
* Convolutional layers
* ReLU activation
* Max Pooling
* Flatten layer
* Fully connected (Dense) layers
* Softmax output layer
* Model compilation
* Model training
* Model evaluation
* Error analysis

## 🧠 CNN Architecture

The implemented CNN consists of:

```text
Input Image
   ↓
Conv2D (32 filters, 3×3)
   ↓
MaxPooling2D
   ↓
Conv2D (64 filters, 3×3)
   ↓
MaxPooling2D
   ↓
Flatten
   ↓
Dense (128 neurons)
   ↓
Dense (10 classes, Softmax)
```

## 📊 Model Evaluation

The model was evaluated using multiple classification metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

The confusion matrix was also analyzed using class names to identify which CIFAR-10 classes were more frequently confused by the model.

## 🔍 Error Analysis

Misclassified samples were analyzed to understand common classification errors and identify visually similar classes.

This analysis helps in understanding model limitations and possible areas for improvement.

## 🛠️ Technologies & Libraries

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Google Colab

## 📁 Repository Contents

```text
CIFAR-10_CNN_Image-Classification/
│
├── Image_classification_model.ipynb
├── final_cifar10_cnn.keras
└── README.md
```

### Files

**`Image_classification_model.ipynb`**
Complete project notebook containing dataset exploration, preprocessing, augmentation, CNN architecture, training, evaluation, visualizations, and error analysis.

**`final_cifar10_cnn.keras`**
Saved trained Keras model.

## 📚 Dataset

The project uses the **CIFAR-10 dataset**, which contains 60,000 color images of size 32×32 pixels across 10 classes.

* 50,000 training images
* 10,000 test images
* 10 classes
* Image shape: 32 × 32 × 3

## 🎯 Learning Objectives

Through this project, the following concepts were practiced:

* Understanding image classification
* Preparing image datasets for deep learning
* Applying image normalization and augmentation
* Building CNN architectures
* Understanding convolution and pooling
* Training deep learning models
* Evaluating classification performance
* Interpreting confusion matrices
* Performing basic error analysis

## 🚀 Future Improvements

Possible improvements include:

* Experimenting with deeper CNN architectures
* Hyperparameter tuning
* Applying regularization techniques
* Comparing different optimizers and learning rates
* Using transfer learning
* Improving performance through additional augmentation
* Deploying the trained model as an image classification application

## 👩‍💻 Project

**Developed by:** Lubna Naseer
**Project:** CIFAR-10 CNN Image Classification
