# CVPR Assignment: CNN Development on Custom Image Dataset

## 📌 Project Overview

This project presents the development of a **custom Convolutional Neural Network (CNN)** implemented from scratch using PyTorch for multi-class image classification. The objective is to train a deep learning model capable of learning meaningful visual patterns and accurately classifying images into predefined categories.

The model was trained and evaluated using the CIFAR-10 dataset, and different regularization techniques such as **Batch Normalization** and **Dropout** were incorporated to improve generalization and reduce overfitting.

---

## ⚠️ Important Note Regarding Model Weights (.pth)
the model weight file (model_path.pth) store in github.


* The file can be downloaded securely and loaded into the notebook for inference or evaluation.

---

## 📊 Dataset Description & Preparation

### 1. Dataset Source

The dataset used in this project is **CIFAR-10**, a standard benchmark dataset widely used in computer vision tasks.

* Total Images: 60,000
* Training Images: 50,000
* Test Images: 10,000
* Number of Classes: 10
* Image Size: 32×32 RGB

### 2. Data Preprocessing

To enhance performance and stability, the following preprocessing steps were applied:

* **Normalization:** Standard CIFAR-10 mean and standard deviation
* **Data Augmentation:**

  * Random cropping
  * Horizontal flipping
* **Resizing:** Maintained original 32×32 resolution
* **Conversion:** Images converted to PyTorch tensors

### 3. Data Splitting

The dataset was split as follows:

* Training Set: 90% of training data
* Validation Set: 10% of training data
* Test Set: Official CIFAR-10 test split

---

## 🧠 Model Architecture

A custom CNN architecture was designed with the following components:

### 🔹 Feature Extraction Layers

* 3 Convolutional blocks:

  * Conv2D → BatchNorm → ReLU → MaxPooling
* Increasing feature depth: 32 → 64 → 128 channels

### 🔹 Regularization Techniques

* **Batch Normalization:** Stabilizes training and speeds convergence
* **Dropout Layers:** Prevents overfitting (0.25–0.5)

### 🔹 Fully Connected Layers

* Flatten layer
* Dense layer (256 neurons)
* Output layer (10 classes)

---

## ⚙️ Training Configuration

* **Loss Function:** CrossEntropyLoss
* **Optimizer:** Adam (learning rate = 0.001)
* **Learning Rate Scheduler:** StepLR (step size = 5, gamma = 0.5)
* **Batch Size:** 128
* **Epochs:** 15

---

## 📈 Results & Evaluation

The model demonstrated strong performance on unseen test data.

### 🔹 Overall Performance

* **Test Accuracy:** ~75–85% (depending on training duration)
* **Loss Trend:** Smooth convergence with minimal overfitting

### 🔹 Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-score

### 🔹 Class-wise Performance

* **Best Performing Classes:** Airplane, Ship (distinct features)
* **Worst Performing Classes:** Cat, Dog (high visual similarity)

---

## 📊 Confusion Matrix Analysis

The confusion matrix reveals that:

* The model performs well on visually distinct objects
* Misclassifications occur between classes with similar textures and shapes

  * Example: Cat vs Dog
  * Example: Deer vs Horse

---

## 🧪 Overfitting & Regularization Analysis

The use of **Batch Normalization** and **Dropout** significantly improved model generalization:

* Training and validation loss remained closely aligned
* No severe overfitting observed
* Model generalized well to unseen test data

---

## 📁 Repository Structure

* `CNN_StudentID.ipynb`
  → Full implementation including preprocessing, training, and evaluation

* `cnn_cifar10_best.pth`
  → Saved best model weights

* `cnn_cifar10_final.pth`
  → Final trained model

* `Model_weight.txt`
  → Contains Google Drive link for large model file

* `README.md`
  → Project documentation

---

## 🚀 Future Improvements

* Use deeper architectures (e.g., ResNet)
* Apply advanced data augmentation
* Perform hyperparameter tuning
* Implement transfer learning

---

## 📌 Conclusion

This project successfully demonstrates the implementation of a custom CNN for image classification. The model effectively learns hierarchical visual features and achieves strong classification performance.

The use of regularization techniques ensures robust generalization, making the model reliable for unseen data. This assignment highlights the practical application of CNNs in real-world computer vision problems.

---

**End of Report**
