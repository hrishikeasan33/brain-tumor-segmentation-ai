# 🧠 Advanced Brain Tumor Segmentation & Localization

An open-source AI framework for automated brain tumor segmentation, localization, and statistical analysis using MRI data. Powered by Attention U-Net, this system detects tumors, identifies their anatomical location, estimates severity and area, and allows mask export in real-time through a Gradio interface.

---

## 🚀 Demo Interface

![image](https://github.com/user-attachments/assets/d23be267-db4c-4383-aa47-dc17e529cb29)
once we upload the image it will detect and give us we can able to download the predicted mask 
![image](https://github.com/user-attachments/assets/6b2a7d4e-e782-402c-af07-f71bdd1eecdd)



---

## 🧩 Dataset and Preprocessing

We used open-source neuroimaging data (MRI) and processed it with the following pipeline:

![Preprocessing Pipeline]![image](https://github.com/user-attachments/assets/73d184ac-2148-4527-9274-3b383e9e7c4d)


Steps involved:
- Normalized pixel intensities  
- Applied affine transforms for augmentation  
- Removed blank masks  
- Resized images to 128×128 resolution  

---

## 🧠 Model Architecture

The core model is an **Attention U-Net**. Here's how the architecture and output flow works:

![Model Pipeline]![image](https://github.com/user-attachments/assets/dab76e53-f70b-4d3c-8cc3-a53758bf7801)


Key components:
- Attention gates for focus on tumor regions  
- Pixel-wise segmentation  
- Overlays + heatmaps  
- Bounding box and quadrant label inference  

---

## 📊 Statistical Analysis

We performed hypothesis testing between **true tumor areas** and **predicted tumor areas**:

![Statistical Tests]![image](https://github.com/user-attachments/assets/9f41797b-66c3-4c8d-a595-95a4dc1b15c9)


```text
T-test p-value: 0.00073
ANOVA p-value: 0.00073

