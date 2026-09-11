

# CodeAlpha Handwritten Character Recognition

## Project Overview

This project implements a **Handwritten Character Recognition system** using a **Convolutional Neural Network (CNN)** and the **MNIST handwritten digit dataset**.

The model is trained to recognize handwritten digits from **0 to 9**.

## Objectives

- Load and explore the MNIST dataset
- Preprocess handwritten digit images
- Build a CNN-based deep learning model
- Train and validate the model
- Evaluate model performance
- Generate a confusion matrix and classification report
- Visualize correct and incorrect predictions
- Test the trained model using real-world handwritten digit images

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Dataset

The project uses the **MNIST handwritten digit dataset**.

- Training images: 60,000
- Testing images: 10,000
- Image size: 28 × 28 pixels
- Number of classes: 10
- Classes: 0–9

## CNN Architecture

The CNN model consists of:

1. Input Layer
2. Convolutional Layer – 32 filters
3. Max Pooling Layer
4. Convolutional Layer – 64 filters
5. Max Pooling Layer
6. Flatten Layer
7. Dense Layer – 128 neurons
8. Dropout Layer – 0.3
9. Output Layer – 10 neurons with Softmax activation

## Model Training

The model was trained using:

- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy
- Epochs: 10
- Batch Size: 128
- Validation Split: 10%

## Results

The trained CNN achieved:

**Test Accuracy: 99.28%**

The model performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Classification Report

## Real-World Testing

The trained model can also be tested using handwritten digit images uploaded from a computer.

The uploaded image is:

1. Converted to grayscale
2. Preprocessed
3. Cropped to the handwritten digit
4. Resized to 28 × 28 pixels
5. Normalized
6. Passed to the trained CNN model

The model then predicts the handwritten digit and displays its confidence score.

## Google Colab
https://colab.research.google.com/drive/1DOdTS6nn9j3RUcW6g-Ota3pD45IgPXGj?usp=sharing 

## Project Structure

```text
CodeAlpha_Handwritten-Character-Recognition/
│
├── CodeAlpha_Handwritten_Character_Recognition.ipynb
├── README.md
├── requirements.txt
│
└── results/
    ├── classification_report.csv
    ├── confusion_matrix.csv
    ├── confusion_matrix.png
    ├── model_performance.csv
    ├── sample_predictions.csv
    ├── training_history.csv
    ├── training_validation_accuracy.png
    └── training_validation_loss.png
