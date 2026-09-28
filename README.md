# CIFAR-10 Image Classification using CNN

## Project Overview

A deep learning image classification project developed using **TensorFlow/Keras** to classify CIFAR-10 images into 10 object categories. The project covers the complete machine learning workflow, from data preprocessing and CNN development to evaluation, error analysis, and model improvement.

## Objective

The objective was to build a CNN-based image classifier, evaluate its performance using multiple classification metrics, analyze model weaknesses, and improve generalization through data augmentation.

## Dataset

**CIFAR-10** was used, containing:

* 50,000 training images
* 10,000 test images
* Image size: `32 × 32 × 3`
* 10 classes
* 5,000 images used for validation from the training set

### Classes

`airplane` · `automobile` · `bird` · `cat` · `deer` · `dog` · `frog` · `horse` · `ship` · `truck`

## Preprocessing

* Split training data into training and validation sets
* Normalized pixel values to the range `[0, 1]`
* Verified image shapes and class labels
* Prepared data for CNN training

## Data Augmentation

To reduce overfitting and improve generalization, **Random Horizontal Flip** augmentation was introduced in the improved model.

## CNN Architecture

The model uses a lightweight CNN architecture:

```text
Input (32×32×3)
      ↓
Conv2D (32 filters, 3×3) + ReLU
      ↓
MaxPooling (2×2)
      ↓
Conv2D (64 filters, 3×3) + ReLU
      ↓
MaxPooling (2×2)
      ↓
Flatten
      ↓
Dense (128) + ReLU
      ↓
Dense (10) + Softmax
```

**Total parameters:** 545,098

The model was compiled using:

* **Optimizer:** Adam
* **Loss:** Sparse Categorical Crossentropy
* **Metric:** Accuracy

## Training

The CNN was trained for **20 epochs** with a batch size of **32**.

Two experiments were performed:

1. **Baseline CNN**
2. **Improved CNN with RandomFlip augmentation**

## Evaluation

Performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Classification report
* Confusion matrix

## Results

| Metric              | Baseline |   Improved |
| ------------------- | -------: | ---------: |
| Validation Accuracy |   68.88% |     73.04% |
| Test Accuracy       |   67.91% | **72.00%** |
| Precision           |   68.39% | **72.39%** |
| Recall              |   67.91% | **72.00%** |
| F1-score            |   68.04% | **71.91%** |

The improved model increased test accuracy by **4.09 percentage points**.

The training-validation gap decreased from **28.26 to 16.67 percentage points**, indicating reduced overfitting and improved generalization.

## Confusion Matrix

The confusion matrix was used to analyze class-level predictions and identify patterns of misclassification.

The baseline model showed higher confusion among visually similar classes, particularly **cat, dog, bird, and deer**.

The confusion matrix visualization is included in the project materials.

## Error Analysis

Misclassification analysis identified:

* Significant confusion between visually similar animal classes
* Cat, dog, bird, and deer as challenging categories
* Overfitting in the baseline model
* Difficulty distinguishing classes with similar visual features

## Model Improvement

**Random Horizontal Flip augmentation** was integrated into the CNN training pipeline.

After retraining:

* Test accuracy improved from **67.91% → 72.00%**
* Precision improved from **68.39% → 72.39%**
* F1-score improved from **68.04% → 71.91%**
* Train-validation gap decreased substantially

This demonstrated that data augmentation improved the model's generalization on unseen images.

## Limitations

* CIFAR-10 images are very small (`32×32`), limiting fine-grained visual information.
* The baseline CNN has limited depth and capacity.
* Some visually similar classes remain difficult to distinguish.
* Further regularization and architectural improvements could potentially improve performance.

## Future Work

Potential improvements include:

* Deeper CNN architectures
* Batch Normalization
* Dropout and additional regularization
* Learning-rate scheduling
* More advanced data augmentation
* Transfer learning with pretrained models
* Hyperparameter tuning
* Evaluation with additional model architectures

## How to Run

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <REPOSITORY_NAME>
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the notebook

Open:

```text
CIFAR10_CNN_Image_Classification.ipynb
```

Run the notebook from beginning to end.

### 4. Trained Model

The final trained model is saved in Keras format:

```text
final_cifar10_cnn.keras
```

It can be loaded using:

```python
from tensorflow import keras

model = keras.models.load_model("final_cifar10_cnn.keras")
```

## Project Structure

```text
CIFAR-10-CNN/
│
├── CIFAR10_CNN_Image_Classification.ipynb
├── final_cifar10_cnn.keras
├── visualizations/
│   ├── training_curves.png
│   ├── confusion_matrix.png
│   └── misclassified_images.png
├── requirements.txt
└── README.md
```

## Technologies

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Google Colab / Jupyter Notebook

## Author

**Lubna Naseer**

Computer Science Graduate | AI/ML Enthusiast
