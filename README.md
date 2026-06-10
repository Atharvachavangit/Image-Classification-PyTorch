# Image-Classification-PyTorch
Built an image classification system using a custom Convolutional Neural Network (CNN) in PyTorch, trained on the CIFAR-10 dataset (60,000 images, 10 classes). Achieved ~70% test accuracy using SGD optimizer with momentum, data normalization, and max pooling. Deployed the model for real-time inference on custom images.


# CIFAR-10 Image Classifier using CNN (PyTorch)

A deep learning project that builds, trains, and evaluates a Convolutional Neural Network (CNN) from scratch to classify images from the CIFAR-10 dataset into 10 categories.

---

## 📌 Project Overview

This project implements an end-to-end image classification pipeline using PyTorch. The model is trained on 60,000 labeled images across 10 classes and evaluated on 10,000 test images.

---

## 🗂️ Dataset

- **Name:** CIFAR-10
- **Classes:** Plane, Car, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck
- **Training images:** 50,000
- **Test images:** 10,000
- **Image size:** 32x32 RGB

---

## 🧠 Model Architecture

| Layer | Details |
|---|---|
| Conv1 | 3 → 12 filters, kernel 5x5 |
| MaxPool | 2x2 |
| Conv2 | 12 → 24 filters, kernel 5x5 |
| MaxPool | 2x2 |
| FC1 | 600 → 120 |
| FC2 | 120 → 84 |
| FC3 | 84 → 10 (output) |

- **Activation Function:** ReLU
- **Loss Function:** Cross Entropy Loss
- **Optimizer:** SGD (lr=0.001, momentum=0.9)
- **Epochs:** 30
- **Batch Size:** 32

---

## 🛠️ Requirements

```
Python 3.x
PyTorch
torchvision
Pillow
NumPy
```

Install dependencies:

```bash
pip install torch torchvision pillow numpy
```

---

## 🚀 How to Run

**1. Clone the repository**
```bash
git clone https://github.com/yourusername/cifar10-cnn.git
cd cifar10-cnn
```

**2. Train the model**
```bash
jupyter notebook train.ipynb
```

**3. Run inference on custom images**
```bash
# Place your images in the project folder and update image_paths in the notebook
image_paths = ['your_image.jpg']
```

---

## 📊 Results

| Metric | Value |
|---|---|
| Test Accuracy | ~70% |
| Training Epochs | 30 |
| Optimizer | SGD |

---

## 📁 Project Structure

```
cifar10-cnn/
│
├── data/                  # CIFAR-10 dataset (auto-downloaded)
├── train.ipynb            # Training notebook
├── trained_net.pth        # Saved model weights
├── README.md              # Project documentation
```

---

## 🔮 Future Improvements

- Add data augmentation (random flips, crops)
- Try Adam optimizer
- Experiment with deeper architectures (ResNet, VGG)
- Deploy as a web app using Flask or Streamlit

---


