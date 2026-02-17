# MNIST & FashionMNIST Models

This repository contains two simple PyTorch examples for image classification:

1. **Fully Connected Neural Network on MNIST**
2. **Convolutional Neural Network (CNN) on FashionMNIST**

---

## 1. MNIST - Fully Connected Network

* **Dataset**: [MNIST](http://yann.lecun.com/exdb/mnist/) handwritten digits (28×28 grayscale images)
* **Model**:

  * Flatten input → Linear(784→128) → ReLU → Linear(128→10)
* **Loss**: `CrossEntropyLoss`
* **Optimizer**: `SGD` (lr=0.01)
* **Training**: 5 epochs, batch size 64
* **Results**:

  * Training loss decreased from 1.216 → 0.330
  * Test accuracy: ~91.5%

---

## 2. FashionMNIST - Convolutional Neural Network

* **Dataset**: [FashionMNIST](https://github.com/zalandoresearch/fashion-mnist) (28×28 grayscale images)
* **Model Architecture**:

  * Conv2d(1→8) → ReLU → MaxPool(2×2)
  * Conv2d(8→16) → ReLU → MaxPool(2×2)
  * Flatten → Linear(16×7×7→128) → ReLU → Linear(128→10)
* **Loss**: `CrossEntropyLoss`
* **Optimizer**: `Adam` (lr=0.002)
* **Training**: 5 epochs, batch size 32
* **Results**:

  * Training loss decreased from 0.429 → 0.197
  * Test accuracy: ~90.85%
## Notes

* MNIST is grayscale digits, FashionMNIST is grayscale clothing items.
* Fully connected networks are good for simple datasets; CNNs perform better on images because they capture spatial features.
