# 🧬 Blood Cell Cancer Classification using Deep Learning

## 📌 Project Overview
This project focuses on the classification of blood cell microscopic images into **benign and malignant cancer subtypes** using deep learning techniques.

The goal is to build an accurate and reliable model that can assist in **early detection and classification of blood cancer**.

The project includes:
- Data preprocessing  
- Exploratory analysis  
- Model development  
- Performance evaluation  
- Web application deployment  

---

## 📂 Dataset Description

The dataset consists of microscopic blood cell images categorized into four classes:

| Class | Type | Number of Images |
|------|------|------------------|
| Benign | Non-cancerous | 512 |
| Early Pre-B | Malignant | 979 |
| Pre-B | Malignant | 955 |
| Pro-B | Malignant | 796 |

---

## 🔍 Data Preprocessing & Exploration

The following steps were performed to ensure data quality and consistency:

### ✔ Data Loading & Visualization
- Loaded images from directory structure  
- Visualized sample images from each class  
- Verified correct class labeling  

### ✔ Data Cleaning
- Checked for duplicate images  
- Removed duplicates (if present)  

### ✔ Image Standardization
- Checked image dimensions  
- Resized all images to **224 × 224 pixels**  

### ✔ Normalization
- Scaled pixel values from **[0–255] to [0–1]**  

### ✔ Data Splitting
- Training set: **70%**  
- Validation set: **15%**  
- Test set: **15%**  

### ✔ Class Balance Check
- Verified class distribution across all splits  

---

## ⚙️ Image Data Generators

Image generators were used for efficient data loading and preprocessing.

### Key functionalities:
- Load images directly from file paths  
- Resize images automatically  
- Normalize pixel values  
- Apply real-time **data augmentation**  
- Generate batches for training  

Separate generators were created for:
- Training  
- Validation  
- Testing  

---

## 🧠 Model Development

Four deep learning models were implemented and compared:

### 🔹 Custom CNN
- Designed and built from scratch  
- Used as a baseline model  

### 🔹 VGG19 (Transfer Learning + Fine-Tuning)
- Utilizes pre-trained **VGG19** architecture (ImageNet)  
- Fine-tuned for this classification task  
- **Achieved the best performance**  

### 🔹 EfficientNetB0 (Transfer Learning + Fine-Tuning)
- Efficient architecture with balanced scaling  
- Fine-tuned for improved accuracy  

### 🔹 MobileNetV2 (Transfer Learning + Fine-Tuning)
- Lightweight and fast architecture  
- Suitable for resource-constrained environments  

---

## 📊 Model Performance Comparison

| Model | Accuracy | Precision | Recall | F1 Score | AUC |
|------|----------|----------|--------|----------|------|
| CNN | 0.925 | 0.924 | 0.925 | 0.923 | 0.986 |
| VGG19 | **0.985** | **0.986** | **0.985** | **0.985** | **0.999** |
| MobileNetV2 | 0.923 | 0.930 | 0.923 | 0.923 | 0.994 |
| EfficientNetB0 | 0.944 | 0.947 | 0.944 | 0.944 | 0.994 |

---

## 🏆 Best Model Selection
- **VGG19** achieved the highest performance across all metrics  
- Selected as the final model for deployment  

---

## 🚀 Web Application

A web application was developed using Flask to classify new blood cell images.

### 🔮 Prediction Output
The model predicts whether an input image belongs to:
- Benign  
- Malignant Early Pre-B  
- Malignant Pre-B  
- Malignant Pro-B  

---

## 🛠️ Tech Stack
- Python  
- TensorFlow / Keras  
- NumPy, Pandas  
- Matplotlib  
- Flask  


## 📦 Model Download

The trained model is large and not included in this repository.

Download it here:
👉 [Download Model](PASTE_YOUR_GOOGLE_DRIVE_LINK)
