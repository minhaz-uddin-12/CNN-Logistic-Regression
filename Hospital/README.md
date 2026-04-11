# Pneumonia Detection using CNN (Chest X-Ray Images)

## Overview
This project aims to develop a **Convolutional Neural Network (CNN)** model to classify chest X-ray images into two categories:
* **Pneumonia**
* **Normal**
The model is trained on a dataset of pediatric chest X-ray images and is designed to assist in medical image classification.

## Dataset Description
The dataset contains:
* **5,863 X-ray images (JPEG format)**
* Organized into:
  * `train/` → Training data
  * `val/` → Validation data
  * `test/` → Testing data

Each folder has two classes:
* `PNEUMONIA`
* `NORMAL`

## Methodology
### Data Preprocessing
* Images are resized to **150 × 150 pixels**
* Pixel values are normalized using `rescale = 1/255`
* Data augmentation applied on training data:
  * Zoom
  * Shear
  * Horizontal flip

### Model Architecture (CNN)
The model is built using multiple layers:
1. **Convolution Layers (Conv2D)**
   Extract important features from images
2. **MaxPooling Layers**
   Reduce image size and computation
3. **Flatten Layer**
   Converts 2D data into 1D
4. **Dense Layer**
   Learns patterns and relationships
5. **Dropout Layer (0.6)**
   Reduces overfitting
6. **Output Layer (Sigmoid)**
   Used for binary classification

### Model Compilation

* Optimizer: **Adam (learning rate = 0.0001)**
* Loss Function: **Binary Crossentropy**
* Evaluation Metric: **Accuracy**

### Training
* Model trained for **12 epochs**
* Validation data used to monitor performance during training

## Results

| Metric              | Accuracy |
| ------------------- | -------- |
| Training Accuracy   | ~92–94%  |
| Validation Accuracy | ~85–87%  |
| Test Accuracy       | ~89–90%  |

## Findings
* Validation accuracy shows slight fluctuations during training
* This is due to the **small size of the validation dataset**
* Despite this, the model performs well on unseen test data

## Tools & Technologies
* Python
* TensorFlow / Keras
* Google Colab
* Matplotlib

## Conclusion
The CNN model successfully classifies chest X-ray images with high accuracy.
It demonstrates good performance and generalization ability for medical image classification tasks.

## Future Improvements
* Use larger validation dataset for better stability
* Apply advanced models (e.g., Transfer Learning)
* Tune hyperparameters for improved accuracy
