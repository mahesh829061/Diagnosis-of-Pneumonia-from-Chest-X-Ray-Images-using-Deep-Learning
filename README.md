# 🩺 Pneumonia Detection from Chest X-Ray Images using Deep Learning

## 📌 Overview
This project focuses on the **automated detection of Pneumonia from Chest X-Ray (CXR) images** using **Deep Learning** techniques.  
A comparative analysis is performed between:

- **CNN trained from scratch**
- **Transfer Learning using a pre-trained ResNet50 model**

---

## 🎯 Objectives
- Build a baseline CNN model trained from scratch
- Implement transfer learning using ResNet50
- Handle medical data scarcity and class imbalance
- Compare performance using standard evaluation metrics
- Demonstrate the importance of transfer learning in medical imaging

---

## 📂 Repository Structure
<pre>
📂 Repository Structure
├── CNN from Scratch.ipynb # Custom CNN model
├── Transfer Learning.ipynb # ResNet50 transfer learning model
├── Report.pdf
├── Dataset
├── README.md
</pre>


---

## 📊 Dataset
**Dataset:** Kaggle Chest X-Ray Images (Pneumonia)

- Total images: ~6,000
- Classes:
  - `0` → Normal
  - `1` → Pneumonia

### 🖼️ Sample Chest X-Ray Images
<img width="1481" height="1119" alt="image" src="https://github.com/user-attachments/assets/a3d50743-8dd7-4c44-885f-65eea82946c7" />


---

## 📈 Dataset Distribution

| Split      | Normal | Pneumonia | Total |
|------------|--------|-----------|-------|
| Training   | 1343   | 3875      | 5218  |
| Testing    | 234    | 390       | 624   |
| Validation | 8      | 8         | 16    |

### 📊 Class Distribution Visualization
<img width="797" height="609" alt="image" src="https://github.com/user-attachments/assets/9b531417-a9b2-4563-b164-bb60feefbbe3" />
### 
<img width="787" height="590" alt="image" src="https://github.com/user-attachments/assets/2dc94b58-7d70-4775-8548-c3023cb35848" />
### 
<img width="774" height="601" alt="image" src="https://github.com/user-attachments/assets/8ce22dea-a156-44cc-8c33-b693fa69038a" />


---

## 🛠️ Data Preprocessing
- Resize images to **224 × 224**
- Convert grayscale images to **3-channel RGB**
- Normalize pixel values
- Data augmentation:
  - Rotation
  - Horizontal flipping
  - Zoom

---

## ⚖️ Class Imbalance Handling
Class weighting was applied during training:

- **Normal (Class 0): 1.94**
- **Pneumonia (Class 1): 0.67**

This prevents model bias toward the majority class.

---

## 🧪 Model Architectures

### 1️⃣ CNN Trained from Scratch
- Convolutional layers with ReLU
- MaxPooling layers
- Fully connected Dense layers
- Sigmoid activation for binary classification

#### 📉 Training Performance (CNN from Scratch)
<img width="589" height="878" alt="image" src="https://github.com/user-attachments/assets/7ee0947f-2a2b-4e8f-9a5a-ac02cb9a6a06" />


---

### 2️⃣ Transfer Learning with ResNet50
- Pre-trained on ImageNet
- Early layers frozen
- Custom classification head
- Fine-tuned with low learning rate

#### 📉 Training Performance (ResNet50)
<img width="565" height="878" alt="image" src="https://github.com/user-attachments/assets/46dce076-f296-4069-ba72-8ff1250de55d" />


---

## 📐 Evaluation Metrics
- Accuracy
- Precision
- Recall (Sensitivity)
- F1-Score
- ROC-AUC

---

## 📊 Results

|            Model             |  Accuracy | Precision | Recall | F1-Score |
|------------------------------|-----------|-----------|--------|----------|
| CNN from Scratch             |   0.894   |   0.615   |  0.631 |  0.623   |
| ResNet50 (Transfer Learning) | **0.901** |   0.612   |  0.608 |  0.610   |

---

## 🔍 Key Findings
- Training CNNs from scratch is difficult for medical datasets
- Transfer learning improves generalization
- Class weighting enhances robustness
- ResNet50 converges faster and more stably


---


