# 🩻 Mammogram Classification using Transformer Models

This repository provides implementations of transformer-based deep learning models for binary classification of mammogram images—distinguishing between malignant and benign tumors. It includes three unique transformer architectures, each with different strengths and performance characteristics.

---

## 🔍 Models Overview

### 1. SwinTransformer_V2

An enhanced version of the original Swin Transformer, specifically fine-tuned for mammogram classification.

**Training Details:**
- **Epochs:** 50
- **Train Accuracy:** 91.91%  
- **Validation Accuracy:** 83.14%  
- **Test Performance:**
  - Precision: Class 0 (0.94), Class 1 (0.77)
  - Recall: Class 0 (0.75), Class 1 (0.95)
  - F1-Score: Class 0 (0.83), Class 1 (0.85)
  - Overall Accuracy: 0.84
  - Macro Avg: Precision (0.86), Recall (0.85), F1-Score (0.84)
  - Weighted Avg: Precision (0.86), Recall (0.84), F1-Score (0.84)

**Confusion Matrix:**
- True Positives (Malignant): 239  
- False Negatives (Missed Malignant): 81  
- False Positives (Benign Misclassified): 14  
- True Negatives (Benign): 266

**Model Size:** 38.9 KB (355 lines of code)

---

### 2. MVSwinTransformer

A multi-view Swin Transformer variant that leverages multiple mammogram perspectives for classification.

**Training Details:**
- **Epochs:** 10  
- **Accuracy:** Increased from 52.48% to 98.86%  
- **Final Test Accuracy:** 99.93%  
- **Precision:** 0.9990  
- **Recall:** 0.9995  
- **F1 Score:** 0.9993  

**Confusion Matrix:**
[[2057 2] [ 1 2071]]
**Model Size:** 88.8 KB (1688 lines of code)

---

### 3. SwinTransformer (Base)

The foundational Swin Transformer architecture adapted for mammogram classification.

**Training Details:**
- **Epochs:** 50  
- **Validation Accuracy:** 96.30%  
- **Loss:** 0.1387  
- **Top-5 Accuracy:** 1.0000  
- **Test Accuracy:** 96.00%  

**Classification Report:**
- Class 0: Precision (0.97), Recall (0.97), F1-Score (0.97)
- Class 1: Precision (0.94), Recall (0.93), F1-Score (0.94)

**Confusion Matrix:**
[[236 7] [ 8 115]]
**Model Size:** 111 KB (1102 lines of code)

---

## 📊 Performance Comparison

| Model               | Accuracy | Precision | Recall | F1-Score | Training Epochs |
|--------------------|----------|-----------|--------|----------|-----------------|
| **MVSwinTransformer** | 99.93%   | 0.9990    | 0.9995 | 0.9993   | 10              |
| **SwinTransformer**   | 96.00%   | 0.96      | 0.96   | 0.96     | 50              |
| **SwinTransformer_V2**| 84.00%   | 0.86      | 0.84   | 0.84     | 5               |

---

## 💡 Key Insights

1. **MVSwinTransformer** delivers near-perfect accuracy with fewer training epochs, demonstrating the power of multi-view learning in mammography.
2. **SwinTransformer (Base)** achieves high accuracy (96%) with extensive training.
3. **SwinTransformer_V2** shows promise with just 5 epochs—suggesting potential with further training and tuning.

---

## 🚀 Usage

Each model is available in a dedicated Collab notebook:
- `SwinTransformer.ipynb`
- `SwinTransformer_V2.ipynb`
- `MVSwinTransformer.ipynb`

