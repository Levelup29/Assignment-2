
# 🚗 Car Model Prediction using Deep Learning  

## 📌 Project Overview  
This project implements **car model classification** using **deep learning and transfer learning**.  
It fine-tunes **VGG-19** to classify images of different car models.

---

## 🚀 Features  
- ✅ **Pre-trained CNN Model** (VGG-19)  
- ✅ **Data Augmentation & Preprocessing**  
- ✅ **Fine-tuning for Improved Accuracy**  
- ✅ **Performance Metrics & Evaluation**  

---

## 📂 Dataset  
**Dataset:** Custom Car Model Image Dataset  
- **Classes:** Various Car Models  
- **Split:** 70% Training, 20% Validation, 10% Testing  

---

## ⚙️ Methodology  

### **1️⃣ Data Preprocessing**  
- **Resizing:** 224×224 pixels  
- **Normalization:** Scaling pixel values (0-1)  
- **Data Augmentation:**  
  - Rotation (±25°)  
  - Zoom (0.1)  
  - Horizontal Flipping  

### **2️⃣ Model Selection & Customization**  
- **Base Model:** VGG-19 (Pre-trained on ImageNet)  
- **Custom Layers:**  
  - `GlobalAveragePooling2D()`  
  - `Dense(512, activation='relu')`  
  - `Dropout(0.5)`  
  - `Dense(N_classes, activation='softmax')`  

### **3️⃣ Training & Fine-Tuning**  
- **Phase 1:** Train only custom layers (30 epochs)  
- **Phase 2:** Unfreeze CNN layers and fine-tune (20 epochs)  

### **4️⃣ Evaluation & Results Analysis**  
- **Performance Metrics:**  
  - Accuracy, Precision, Recall  
  - Confusion Matrix  
  - Feature Map Visualization  

---

## 📊 Results  

| Metric               | Before Fine-Tuning | After Fine-Tuning |  
|----------------------|-------------------|-------------------|  
| **Training Accuracy** | 28.41%            | 89.35%            |  
| **Validation Accuracy** | 37.49%          | **74.31%**        |  
| **Test Accuracy**     | -                 | **78.28%**        |  
| **Test Loss**        | -                  | **0.8544**        |  

---

## 🔧 Future Improvements  
- **Data Augmentation Enhancements**  
- **Ensemble Learning for Higher Accuracy**  
- **Hyperparameter Optimization**  

---

## 📌 How to Use  

### 🔹 Install Dependencies  
```bash  
pip install tensorflow keras numpy matplotlib

**🔍 Feature Map Visualization:**  
The model successfully extracts **Car Models**, ensuring **accurate classification**.
