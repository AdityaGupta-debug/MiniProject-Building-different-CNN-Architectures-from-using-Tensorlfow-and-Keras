# 🧠 CNN Models from Scratch

This project implements classic **Convolutional Neural Network (CNN)** architectures from scratch using **TensorFlow** and **Keras**. The goal is to understand the fundamental building blocks of deep learning by recreating landmark CNN models that revolutionized computer vision.

---

## 🎯 Project Overview

Building and training CNN models from scratch helps in understanding:

- 🏗️ Architecture design principles  
- 📉 Parameter efficiency  
- 🧱 Feature extraction hierarchies  
- 🕰️ Historical evolution of deep learning  

---

## 📚 Implemented Models

### 1. 📘 LeNet-5 (1998)

**Overview:**  
Developed by Yann LeCun for handwritten digit recognition (MNIST), LeNet-5 was one of the first successful CNNs and inspired modern architectures.

**Architecture:**

- Input: `32×32 grayscale images`
- Conv1: `6 filters`, `5×5`, no padding
- Pool1: `2×2 average pooling`
- Conv2: `16 filters`, `5×5`, no padding
- Pool2: `2×2 average pooling`
- Flatten
- Dense1: `120 neurons`, `tanh`
- Dense2: `84 neurons`, `tanh`
- Output: `10 neurons` (softmax for digits)

**Key Features:**
- Uses **average pooling**
- **Tanh** activation
- Shallow architecture

**🧮 Total Parameters (~61,706):**
- Conv1: 156  
- Conv2: 2,416  
- Dense1: 48,120  
- Dense2: 10,164  
- Output: 850  

---

### 2. 🏆 AlexNet (2012)

**Overview:**  
Winner of ImageNet ILSVRC 2012, AlexNet was a breakthrough showing deep CNNs' potential for large-scale classification.

**Architecture:**

- Input: `224×224×3` RGB image
- Conv1: `96 filters`, `11×11`, stride 4, ReLU
- MaxPool1: `3×3`, stride 2
- Conv2: `256 filters`, `5×5`, padding, ReLU
- MaxPool2: `3×3`, stride 2
- Conv3: `384 filters`, `3×3`, padding, ReLU
- Conv4: `384 filters`, `3×3`, padding, ReLU
- Conv5: `256 filters`, `3×3`, padding, ReLU
- MaxPool3: `3×3`, stride 2
- Flatten → Dropout(0.5)
- Dense1: `4,096 neurons`, ReLU → Dropout(0.5)
- Dense2: `4,096 neurons`, ReLU → Dropout(0.5)
- Output: `1,000 neurons` (ImageNet)

**Key Innovations:**
- First use of **ReLU** for faster training
- **Dropout** for regularization
- **Data augmentation**
- **GPU training**
- **Local Response Normalization (LRN)**

**🧮 Total Parameters (~62M):**
- Conv Layers: ~3.7M  
- Dense Layers: ~58.6M  

---

### 3. 🔬 VGGNet (2014)

**Overview:**  
Developed by the Visual Geometry Group (Oxford), VGG popularized small (3×3) filters and very deep networks. VGG-16 is one of the most well-known variants.

**VGG-16 Architecture:**

- Input: `224×224×3` RGB
- **Block 1:** 2×Conv (64 filters) → MaxPool  
- **Block 2:** 2×Conv (128 filters) → MaxPool  
- **Block 3:** 3×Conv (256 filters) → MaxPool  
- **Block 4:** 3×Conv (512 filters) → MaxPool  
- **Block 5:** 3×Conv (512 filters) → MaxPool  
- Flatten → Dense1: `4,096 neurons`, ReLU → Dropout(0.5)  
- Dense2: `4,096 neurons`, ReLU → Dropout(0.5)  
- Output: `1,000 neurons`

**Key Features:**
- Uniform architecture with **3×3 conv filters**
- Very **deep network**
- Only **ReLU** activations
- Available in multiple depths: VGG-11/13/16/19

**🧮 Total Parameters (~138M):**
- Conv Layers: ~14.7M  
- Dense Layers: ~123.6M  

---

## 🛠️ Technologies Used

- [TensorFlow 2.x](https://www.tensorflow.org/)
- [Keras](https://keras.io/)
- Python 3.x
- Google Colab / Jupyter Notebooks
