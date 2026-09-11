# Handwritten Character Recognition

## CodeAlpha Machine Learning Internship — Project 2

## Project Overview

This project develops a Convolutional Neural Network (CNN)-based handwritten digit recognition system using the **MNIST handwritten digit dataset**.

The project follows an end-to-end deep learning workflow including dataset loading, data exploration, image preprocessing, CNN model development, model training, validation analysis, performance evaluation, confusion matrix analysis, sample predictions, and real-world handwritten digit testing.

---

## Problem Statement

Handwritten digit recognition is an important computer vision and pattern recognition problem with applications in document processing, postal services, form digitization, automated data entry, and optical character recognition systems.

The objective of this project is to develop a deep learning model capable of recognizing handwritten digits from images.

---

## Dataset

The project uses the **MNIST handwritten digit dataset**.

The dataset contains grayscale images of handwritten digits from **0 to 9**.

Each image has a resolution of:

- 28 × 28 pixels
- 1 grayscale channel
- 10 target classes (digits 0–9)

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow
- Keras
- Google Colab
- GitHub

---

## Project Workflow

The project follows these steps:

1. Project introduction
2. Import libraries
3. Load MNIST dataset
4. Dataset exploration
5. Visualize handwritten digits
6. Image preprocessing
7. Build CNN model
8. Train the model
9. Analyze training and validation performance
10. Evaluate the model on the test dataset
11. Generate confusion matrix
12. Generate sample predictions
13. Save model performance results
14. Perform real-world handwritten digit testing

---

## Data Preprocessing

The handwritten images were prepared for CNN-based classification.

The preprocessing included:

- Normalizing pixel values
- Preparing image dimensions for CNN input
- Converting the images into the required format
- Using the digit labels as classification targets

The CNN receives images with an input shape of **28 × 28 × 1**.

---

## CNN Architecture

The convolutional neural network consists of:

- Input layer
- Convolutional layer with 32 filters
- Max pooling layer
- Convolutional layer with 64 filters
- Max pooling layer
- Flatten layer
- Dense layer with 128 neurons
- Dropout layer
- Output layer with 10 classes

The output layer uses the **Softmax** activation function to produce probabilities for the ten digit classes.

---

## Model Training

The model was compiled using:

- Optimizer: Adam
- Loss function: Sparse Categorical Crossentropy
- Evaluation metric: Accuracy

Training configuration:

- Epochs: 10
- Batch size: 128
- Validation split: 10%

---

## Training Results

The final training results were:

| Metric | Result |
|---|---:|
| Final Training Accuracy | 99.73% |
| Final Training Loss | 0.0082 |
| Final Validation Accuracy | 99.17% |
| Final Validation Loss | 0.0460 |

The training and validation curves were analyzed to observe model learning behavior and generalization performance.

---

## Test Set Performance

The trained CNN was evaluated on the MNIST test dataset.

| Metric | Result |
|---|---:|
| Test Loss | 0.0254 |
| Test Accuracy | 99.28% |

The model achieved high classification accuracy on unseen test images.

---

## Classification Performance

The classification report showed approximately:

- Macro F1-score: **99.27%**
- Weighted F1-score: **99.28%**

The results demonstrate strong performance across the ten handwritten digit classes.

---

## Confusion Matrix

A confusion matrix was generated to analyze the classification performance for each digit class.

It helps identify which digits were correctly classified and which digits were occasionally confused with one another.

The confusion matrix visualization is available in the `results/` directory.

---

## Sample Predictions

The project also generated sample predictions from the test dataset.

For each selected image, the model predicted the corresponding handwritten digit based on the learned visual patterns.

The sample prediction results are saved in:

`results/sample_predictions.csv`

---

## Real-World Handwritten Digit Testing

In addition to evaluating the model on the MNIST test dataset, a handwritten digit was independently tested to demonstrate practical usage.

The handwritten digit image was preprocessed into the required format and passed through the trained CNN model.

The model successfully recognized the tested handwritten digit.

This demonstrates the model's ability to process a handwritten input outside the standard displayed sample predictions.

---

## Results Directory

The following result files were generated:

- `training_history.csv`
- `confusion_matrix.csv`
- `classification_report.csv`
- `sample_predictions.csv`
- `model_performance.csv`
- `training_validation_accuracy.png`
- `training_validation_loss.png`
- `confusion_matrix.png`

---

## Google Colab

The complete implementation is available in Google Colab:

https://colab.research.google.com/drive/1DOdTS6nn9j3RUcW6g-Ota3pD45IgPXGj?usp=sharing

---

## Project Structure

    CodeAlpha_Handwritten-Character-Recognition/
    │
    ├── CodeAlpha_Handwritten_Character_Recognition.ipynb
    ├── README.md
    ├── requirements.txt
    └── results/
        ├── training_history.csv
        ├── confusion_matrix.csv
        ├── classification_report.csv
        ├── sample_predictions.csv
        ├── model_performance.csv
        ├── training_validation_accuracy.png
        ├── training_validation_loss.png
        └── confusion_matrix.png

---

## Conclusion

This project successfully developed a CNN-based handwritten digit recognition system using the MNIST dataset.

The model achieved **99.28% test accuracy**, demonstrating strong performance in recognizing handwritten digits.

The project also included training and validation analysis, classification reporting, confusion matrix visualization, sample predictions, and real-world handwritten digit testing.

Overall, the project demonstrates a complete deep learning workflow for image classification, from data preprocessing and CNN architecture design to model evaluation and practical testing.

---

## Author

**Saripalle Suresh**

Machine Learning Intern — CodeAlpha

## Internship Project

**CodeAlpha Machine Learning Internship — Project 2**
