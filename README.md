# 🌱 Agritex-AI – Smart Farming with Artificial Intelligence  

[![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![PyTorch](https://img.shields.io/badge/PyTorch-1.13-red?logo=pytorch&logoColor=white)](https://pytorch.org/)  
[![OpenCV](https://img.shields.io/badge/OpenCV-Image%20Processing-green?logo=opencv&logoColor=white)](https://opencv.org/)  
[![Arduino](https://img.shields.io/badge/Arduino-Hardware%20Control-00979D?logo=arduino&logoColor=white)](https://www.arduino.cc/)  
[![3D Printing](https://img.shields.io/badge/3D%20Printing-Design-orange?logo=autodesk&logoColor=white)](https://www.autodesk.com/)  


<p align="center">
  <img src="https://github.com/user-attachments/assets/0d1a82b4-9bbb-4909-a68e-0014326be99e" alt="Agritex-AI Banner" width="400"/>
</p>

---

## 🌍 Overview  

**Agritex-AI** is a graduation project from the Faculty of Artificial Intelligence, Kafrelsheikh University (2023–2024).  
It introduces a **smart self-driving agricultural vehicle** powered by **artificial intelligence, computer vision, and precision spraying systems** to revolutionize weed management in farming.  

🔹 **Problem**: Weeds compete with crops for water, nutrients, and sunlight—reducing yields and forcing farmers to overuse pesticides, which harms soil, water, and biodiversity.  

🔹 **Solution**: Agritex-AI leverages **deep learning** and **real-time video processing** to identify weeds, detect their exact coordinates, and spray them with high accuracy using a robotic arm and 3D-printed nozzle.  

### 🚀 Key Impacts  
- Reduce **pesticide usage by up to 90%**  
- Increase **crop yield by ~20%**  
- Protect soil health, pollinators, and the environment  
- Provide farmers with real-time analytics through a connected mobile app  

---
## ✨ Features  

- 🤖 **AI-Powered Weed Detection** – Uses **Convolutional Neural Networks (CNNs)** (MobileNetV3_Small) to identify 12 different crop and weed classes with **99.38% accuracy**.  
- 🎯 **Precision Spraying** – Robotic arm with a **3D-printed nozzle** applies herbicide directly on weeds, reducing chemical use by up to **90%**.  
- 📷 **Real-Time Video Processing** – Detects weed coordinates from live camera feed and maps them for spraying.  
- 🗂 **Data Preprocessing Pipeline** – Custom preprocessing for each crop/weed dataset: segmentation, augmentation, and balancing (3,000 images per class).  
- 🛠 **Hardware Integration** – Built with **Arduino Uno, DC motors, Bluetooth module, and CNC framework** for autonomous navigation and spraying.  
- 📱 **Mobile & Web Applications** – Provides farmers with real-time data, analytics, and field monitoring.  
- 🖨 **3D Printable Designs** – All custom hardware parts (nozzle, arm, vehicle body) are open-source and included in the repository.

---

## 🛠 Technologies Used  

| Technology | Purpose |
|------------|---------|
| ![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python&logoColor=white) | Core programming language |
| ![PyTorch](https://img.shields.io/badge/PyTorch-1.13-red?logo=pytorch&logoColor=white) | Deep learning model training |
| ![OpenCV](https://img.shields.io/badge/OpenCV-Image%20Processing-green?logo=opencv&logoColor=white) | Image preprocessing & segmentation |
| ![Arduino](https://img.shields.io/badge/Arduino-Microcontroller-00979D?logo=arduino&logoColor=white) | Hardware control & automation |
| ![3D Printing](https://img.shields.io/badge/3D%20Printing-Custom%20Designs-orange?logo=autodesk&logoColor=white) | Hardware parts for nozzle & vehicle |
| ![CNC](https://img.shields.io/badge/CNC-Framework-lightgrey?logo=hackaday&logoColor=black) | Precision arm movement |
| ![Bluetooth](https://img.shields.io/badge/Bluetooth-Communication-0082FC?logo=bluetooth&logoColor=white) | Wireless control & connectivity |

---

## 📂 Project Structure  

The repository is organized into the following main folders:  

```
📦 Agritex-AI
┣ 📂 Data Preprocessing
┃ ┗ Scripts for cleaning, segmenting, and preparing datasets for each crop/weed class.
┣ 📂 Models
┃ ┗ Trained deep learning models, including experiments and the best-performing MobileNetV3_Small.
┣ 📂 Video Processing & Coordinates Detection
┃ ┗ Real-time video analysis for weed detection and coordinate mapping.
┣ 📂 3D Designs
┃ ┗ STL/OBJ files for 3D-printed components (nozzle, robotic arm, chassis).
┣ 📂 Documentation
┃ ┗ Full project documentation files.
┣ 📂 Research Paper
┃ ┗ Academic research paper with methodology, results, and references.
┗ README.md (this file)
```
---
## 📊 Dataset  

Agritex-AI was trained on a **comprehensive dataset of ~30,000 images** covering both crops and weeds.  
The dataset was gathered from multiple reliable sources including **PlantVillage, GBIF, Aarhus University, Agricultural University of Athens**, and others (about 39 sources).  

### 🔹 Classes (19 Total)  
- **Crops**: Cotton, Sesame, Wheat, Sugar beet, Tomato, Corn, Strawberry, Beans, cauliflower
- **Weeds**: Convolvulus Arvensis, Euphorbia helioscopia, Euphorbia peplus, Grass, Lolium multiflorum, Nutgrass, Purslane, pigweed, black nightshade, Orobanche crenata forsk

### 🛠 Preprocessing Pipeline 
Each class went through a custom preprocessing stage to ensure high-quality training data:  
- 🌿 **Segmentation** – Isolated plants from their backgrounds using color filtering & morphological operations.  
- 🖼 **Cropping & Splitting** – Split images containing multiple plants, cropped borders, and replaced backgrounds with white.  
- 🔄 **Data Augmentation** – Rotation, flipping, brightness/contrast adjustment, gamma correction, hue & saturation shifts.  
- ⚖ **Balancing** – Fixed dataset size to **3,000 images per class** to address class imbalance.  
- 📐 **Resizing & Normalization** – Resized to `224x224x3`, pixel normalization for better CNN performance.  
- 🧪 **Split** – Training (75%), Validation (15%), Test (15%).  

This preprocessing pipeline ensures **robust generalization** across varied field conditions.  

---
