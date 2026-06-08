# 🐱🐶 Cats vs Dogs Image Classification using SVM

A machine learning project that classifies images of cats and dogs using **HOG Feature Extraction** and **Support Vector Machine (SVM)**.

---

## 📌 Project Overview

This project builds an image classification system from scratch without using deep learning. It demonstrates how raw images can be converted into numerical features and classified using traditional machine learning algorithms.

---

## 📁 Dataset

- **Source:** [Kaggle - Dogs vs Cats](https://www.kaggle.com/datasets/salader/dogs-vs-cats)
- **Total Images:** 24,000
- **Classes:** Cats (12,000) and Dogs (12,000)
- **Format:** JPEG images with varying sizes

```
data/
└── train/
    ├── cats/     ← 12,000 cat images
    └── dogs/     ← 12,000 dog images
```

---

## 🔧 Project Pipeline

```
Raw Images
    ↓
Image Preprocessing (Resize, Grayscale, Normalize)
    ↓
HOG Feature Extraction
    ↓
Dataset Preparation (Labels + Train/Test Split)
    ↓
SVM Training (Linear, RBF, Polynomial)
    ↓
Model Evaluation (Accuracy, Precision, Recall, F1)
```

---

## 📋 Tasks Completed

| Task | Description |
|------|-------------|
| Task 1 | Dataset Understanding and Exploration |
| Task 2 | Image Preprocessing Pipeline |
| Task 3 | HOG Feature Extraction |
| Task 4 | Dataset Preparation and Train/Test Split |
| Task 5 | SVM Classification with 3 Kernels |
| Task 6 | Model Evaluation and Results |

---

## ⚙️ Installation

**1. Clone the repository**
```bash
git clone https://github.com/yourusername/cat-vs-dog-classification.git
cd cat-vs-dog-classification
```

**2. Install required libraries**
```bash
pip install opencv-python
pip install scikit-image
pip install scikit-learn
pip install matplotlib
pip install numpy
pip install pillow
pip install tqdm
```

**3. Download the dataset**

Download from [Kaggle](https://www.kaggle.com/datasets/salader/dogs-vs-cats) and place it as:
```
data/train/cats/
data/train/dogs/
```

**4. Update the dataset path in the code**
```python
DATASET_PATH = r"your/path/to/data/train"
```

---

## 🚀 How to Run

Run each task in order inside Jupyter Notebook or any Python IDE:

```
Task1_Dataset_Understanding.py
Task2_Preprocessing.py
Task3_HOG_Feature_Extraction.py
Task4_Dataset_Preparation.py
Task5_SVM_Classification.py
Task6_Model_Evaluation.py
```

---

## 🖼️ Image Preprocessing

| Step | Details |
|------|---------|
| Resize | 64 x 64 pixels |
| Color | Grayscale |
| Normalization | 0.0 to 1.0 |
| Corrupted Images | Automatically removed |

---

## 🔍 Feature Extraction — HOG

**HOG (Histogram of Oriented Gradients)** captures edge and shape information.

| Parameter | Value |
|-----------|-------|
| Pixels per Cell | 8 x 8 |
| Cells per Block | 2 x 2 |
| Orientations | 9 |
| Feature Vector Size | 1764 per image |

---

## 🤖 SVM Kernels

Three kernel functions were trained and compared:

- **Linear Kernel** — Fast, good baseline performance
- **RBF Kernel** — Best for non-linear image data
- **Polynomial Kernel** — Degree 3 curved boundaries

---

## 📊 Results

| Kernel | Accuracy | Precision | Recall | F1-Score |
|--------|----------|-----------|--------|----------|
| Linear | ~66% | ~66% | ~66% | ~66% |
| RBF | ~71% | ~72% | ~71% | ~71% |
| Polynomial | ~64% | ~65% | ~64% | ~64% |

**Best Performing Kernel: RBF with ~71% accuracy**

---

## 🛠️ Technologies Used

| Library | Purpose |
|---------|---------|
| Python 3.x | Programming language |
| OpenCV | Image reading and processing |
| scikit-image | HOG feature extraction |
| scikit-learn | SVM model training and evaluation |
| NumPy | Array operations |
| Matplotlib | Visualization |
| Pillow | Image format handling |

---

## 📂 Project Structure

```
cat-vs-dog-classification/
│
├── data/
│   └── train/
│       ├── cats/
│       └── dogs/
│
├── Task1_Dataset_Understanding.py
├── Task2_Preprocessing.py
├── Task3_HOG_Feature_Extraction.py
├── Task4_Dataset_Preparation.py
├── Task5_SVM_Classification.py
├── Task6_Model_Evaluation.py
│
└── README.md
```

---

## 📚 What I Learned

- How images are represented as numerical data
- Importance of preprocessing in machine learning pipelines
- How HOG captures structural features from images
- How SVM finds optimal decision boundaries
- Impact of different kernel functions on classification performance
- How to evaluate models using multiple metrics

---

## 📜 License

This project is for educational purposes only.

---

## 🙋 Author

Ania Shams
BS Computer Science Student
