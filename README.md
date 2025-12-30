Here is your content converted into a clean, **professional `README.md` file**, formatted properly for GitHub and academic submission.

---

# 🎙️ Speech Command Classification Using CNN

**Deep Learning CIA – 2**

* **Name:** Haneef Ahmad
* **Class:** IoT – A
* **Roll No.:** 22011102019

---

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** to classify short speech commands into three categories:

* **Yes**
* **No**
* **Don’t Know**

A subset of the **Google Speech Commands Dataset** was used. Audio signals were converted into **spectrograms**, which were then fed into a CNN for classification. The model achieved **high accuracy**, demonstrating the effectiveness of CNNs for lightweight speech recognition tasks, especially in **IoT applications**.

---

## 🧠 Abstract

The goal of this project is to develop a deep learning-based speech recognition system capable of identifying short spoken commands. A CNN model was trained on spectrogram representations of one-second audio clips. The system successfully learned to distinguish between different commands and achieved strong performance, highlighting the potential of CNN-based approaches in real-time and embedded speech recognition systems.

---

## 📖 Introduction

Speech recognition is a key area of **Artificial Intelligence** and **Human–Computer Interaction**, enabling machines to understand and respond to spoken input. It plays a critical role in voice-controlled assistants, smart devices, and IoT systems.

In this assignment, three speech commands were classified using a CNN:

* `"yes"`
* `"no"`
* `"happy"` (used as **“Don’t Know”**)

The focus was on:

* Audio preprocessing
* Feature extraction using spectrograms
* CNN-based classification

---

## 🗂️ Dataset Description

The **Google Speech Commands Dataset** contains over **65,000** one-second audio clips of spoken words.

For this project, only the following folders were used:

* `yes/`
* `no/`
* `happy/` → mapped to **“Don’t Know”**

---

## ⚙️ Data Preprocessing

The following preprocessing steps were applied:

1. Loaded all `.wav` audio files and converted them to **mono**
2. Resampled audio to **16 kHz**
3. Applied **Short-Time Fourier Transform (STFT)** to generate spectrograms
4. Normalized spectrogram values
5. Reshaped data to **128 × 129 × 1**
6. Split dataset into:

   * **80% Training**
   * **20% Testing**

---

## 🏗️ Model Architecture

The CNN architecture used in this project is shown below:

| Layer        | Description                     |
| ------------ | ------------------------------- |
| Input Layer  | Shape: `(128, 129, 1)`          |
| Conv2D       | 16 filters, 3×3 kernel, ReLU    |
| MaxPooling2D | Dimensionality reduction        |
| Conv2D       | 32 filters, 3×3 kernel, ReLU    |
| MaxPooling2D | Further reduction               |
| Flatten      | Converts feature maps to vector |
| Dense        | 128 units, ReLU                 |
| Output Dense | 3 units, Softmax                |

### Compilation Details

* **Optimizer:** Adam
* **Loss Function:** Sparse Categorical Cross-Entropy
* **Metric:** Accuracy

---

## 🏋️ Training Parameters

* **Epochs:** 10
* **Batch Size:** 32
* **Validation Split:** 20%
* **Learning Rate:** 0.001

---

## 📊 Results and Discussion

### 🔹 Model Performance

After training:

* **Training Accuracy:** ~95%
* **Validation Accuracy:** ~90%
* **Test Accuracy:** ~88–92%

The model showed **stable convergence** with minimal overfitting.

---

### 🔹 Confusion Matrix Summary

| Actual \ Predicted | Yes  | No   | Don’t Know |
| ------------------ | ---- | ---- | ---------- |
| **Yes**            | High | Few  | Few        |
| **No**             | Few  | High | Few        |
| **Don’t Know**     | Some | Some | High       |

Most misclassifications occurred between **“No”** and **“Don’t Know”**, likely due to similar energy patterns and short-duration audio features.

---

### 🔹 Training Curves

* Accuracy increased steadily over epochs
* Loss decreased smoothly
* No instability or divergence observed

This confirms proper model learning.

---

## ✅ Conclusion

The CNN model successfully classified short speech commands using **spectrogram-based features**. Despite using a simple architecture and limited data, the model achieved strong accuracy.

This project demonstrates the practicality of deep learning in:

* Speech command recognition
* IoT systems
* Smart home devices
* Embedded applications

---

## 🚀 Future Improvements

Possible enhancements include:

* Data augmentation (noise addition, pitch shifting)
* Using **MFCC** features instead of raw spectrograms
* Applying **transfer learning** with pre-trained audio models

---

## 📎 Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Librosa
* Google Speech Commands Dataset

---

If you want, I can also:

* Make this **shorter for submission**
* Add a **project structure section**
* Convert it into **PDF / DOC format**
* Add **code snippets** to the README
