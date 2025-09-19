# DNN vs LeNet-5 on MNIST

This project compares the performance of a **Deep Neural Network (DNN)** and the **LeNet-5 Convolutional Neural Network (CNN)** on the classic **MNIST handwritten digits dataset**.

## Dataset
- **MNIST**: 60,000 training images and 10,000 test images
- Grayscale, 28×28 pixels
- 10 classes (digits 0–9)

## Model Architectures

### 1. Deep Neural Network (DNN)
- Input: Flatten (28×28)
- Hidden Layers: 2 Dense layers with 128 neurons (ReLU)
- Regularization: Dropout (0.3)
- Output: Dense layer with 10 neurons (Softmax)

### 2. LeNet-5 CNN
- Conv2D → 6 filters (5×5, tanh)
- AveragePooling2D
- Conv2D → 16 filters (5×5, tanh)
- AveragePooling2D
- Flatten
- Dense (120 neurons, tanh)
- Dense (84 neurons, tanh)
- Dense (10 neurons, Softmax)

## Results

| Model | Parameters | Test Accuracy |
|-------|------------|---------------|
| DNN (2 hidden layers + Dropout) | 118,282 | **97.11%** |
| LeNet-5 CNN | 61,706 | **98.76%** |

## Conclusion
- **LeNet-5 CNN** achieves higher accuracy with fewer parameters compared to the DNN.  
- CNNs are more efficient in extracting spatial features from images, making them superior for visual data classification.

## ⚙Tech Stack
- Python
- TensorFlow & Keras
- Google Colab (GPU)

---

You can explore and extend this project by modifying the architectures, adding more layers, or testing with different datasets.

