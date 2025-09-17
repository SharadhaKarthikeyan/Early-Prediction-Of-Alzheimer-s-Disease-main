# Early Prediction of Alzheimer’s Disease Using Machine Learning  

## Overview  
Alzheimer’s Disease (AD) is a progressive neurological disorder that causes memory loss and cognitive decline. Early detection is crucial for effective treatment and patient care.  
This project leverages **ensemble deep learning models (AlexNet + LeNet)** to analyze MRI scans and predict Alzheimer’s Disease at an early stage with **97% accuracy**.  

The system uses MRI data from the **Alzheimer’s Disease Neuroimaging Initiative (ADNI)** and applies preprocessing, feature extraction, and classification to categorize scans into:  
- **AD** – Alzheimer’s Disease  
- **MCI** – Mild Cognitive Impairment  
- **CN** – Cognitively Normal  

---

## Features  
- Ensemble approach combining **AlexNet** and **LeNet** using **majority voting**.  
- High prediction accuracy compared to standalone models.  
- Preprocessing pipeline with **MATLAB (SPM)** and **Python**.  
- Support for MRI visualization (Axial, Coronal, Sagittal views).  
- User-friendly workflow with upload → preprocessing → prediction → prevention guidelines.  

---

## Tech Stack  
- **Languages**: Python, MATLAB  
- **Frameworks/Libraries**: TensorFlow/Keras, NumPy, OpenCV, SPM (for segmentation & normalization)  
- **Dataset**: ADNI (Alzheimer’s Disease Neuroimaging Initiative)  
- **Models Used**:  
  - **AlexNet** (8 layers – 5 convolutional + 3 fully connected)  
  - **LeNet-5** (5 layers – 2 convolutional + 3 fully connected)  
  - **Ensemble Voting Classifier**  

---

## Dataset  
- Source: [Alzheimer’s Disease Neuroimaging Initiative (ADNI)](http://adni.loni.usc.edu/)  
- Data Types: MRI scans (Neuroimaging), PET images, clinical & genetic data  
- In this project, **Coronal MRI slices** are primarily used.  
- Dataset split:  
  - Training: 442 images (AD: 144, MCI: 146, CN: 152)  
  - Testing: 108 images (AD: 36, MCI: 36, CN: 36)  

---

## Workflow  
1. **Upload MRI Scan** (`.nii` format)  
2. **Preprocessing**  
   - Segmentation & Normalization (SPM in MATLAB)  
   - Slicing into Coronal view (Python)  
3. **Model Training & Prediction**  
   - Train AlexNet & LeNet separately (~50 epochs each)  
   - Ensemble via majority voting  
4. **Prediction Output**  
   - Classifies scan as **AD**, **MCI**, or **CN**  
   - Provides probability scores  
5. **Guidelines**  
   - If positive: Prevention & care suggestions  
   - If negative: Risk reduction advice  

---

## Results  
- **AlexNet**: 87% accuracy  
- **LeNet**: 74% accuracy  
- **Ensemble (AlexNet + LeNet)**: **97% accuracy**  

The ensemble approach significantly improves robustness and reliability.  

---
