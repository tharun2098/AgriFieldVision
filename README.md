# 🌾 AgriVision: Smart Crop Detection from Space  

### 🛰️ AI-powered Crop Classification using Sentinel-2 (EuroSAT Dataset)



## 📖 Overview  
AgriVision is a deep learning pipeline that classifies crops and land cover types from satellite imagery.  
Built for **Track 1 – Crop Identification Challenge**, the project demonstrates how **AI + remote sensing** can support precision agriculture, crop monitoring, and yield estimation.  



## 🚀 Features  
- **Data Cleaning & EDA**: Removed corrupted images, explored class distribution, generated correlation heatmaps.  
- **Deep Learning Model**: CNN trained on Sentinel-2 patches from the EuroSAT dataset.  
- **Evaluation**: Accuracy, confusion matrix, classification report.  
- **Visualization**:  
  - Class distribution bar plots  
  - Correlation heatmap of RGB bands  
  - Accuracy/loss training curves  
  - Confusion matrix heatmap  
  - Map-style classification visuals  
- **Prediction Demo**: Upload an image → get predicted crop/land cover name.  



## 📊 Dataset  
- **EuroSAT: Land Use and Land Cover Dataset** (Kaggle)  
- Sentinel-2 image patches (64×64 pixels)  
- 10 classes:  
  `AnnualCrop, Forest, HerbaceousVegetation, Highway, Industrial, Pasture, PermanentCrop, Residential, River, SeaLake`  

[Kaggle Dataset Link](https://www.kaggle.com/datasets/apollo2506/eurosat-dataset)  



## 🛠️ Tech Stack  
- **Python**  
- **Google Colab** (cloud training environment)  
- **TensorFlow / Keras** (CNN model)  
- **Scikit-learn** (metrics & confusion matrix)  
- **Pandas, NumPy** (data handling)  
- **Matplotlib, Seaborn** (visualizations)  
- **OpenCV, PIL** (image preprocessing)  
- **Kaggle API** (dataset access)  



## ⚡ How We Built It  
1. Downloaded EuroSAT dataset from Kaggle using Kaggle API.  
2. Preprocessed data (resized, cleaned, normalized).  
3. Performed EDA (class distribution, correlation heatmap).  
4. Trained CNN model for multi-class classification.  
5. Evaluated with accuracy, F1-score, confusion matrix.  
6. Visualized predictions with both per-image and map-style outputs.  



## 📈 Results  
- Achieved high classification accuracy on EuroSAT test data.  
- Produced interpretable visuals (confusion matrix, heatmaps, map grids).  
- Demonstrated potential to scale pipeline to **AgriFieldNet India** dataset with SAR + optical data.  


### Inspiration  
Small, fragmented farms in India make crop monitoring challenging. We wanted to build an AI system to identify crops from space efficiently.  

### Challenges  
- Handling dataset imbalance  
- Noisy/missing images  
- Limited time for geospatial foundation models  

### Accomplishments  
- End-to-end pipeline (data → model → results → visuals)  
- High accuracy with CNN  
- Clear roadmap to scale beyond EuroSAT  

### What’s Next  
- Extend to **AgriFieldNet India (Track 1)** with SAR + optical time series.  
- Use **foundation models** for generalization.  
- Deploy as a **web app / dashboard** for farmers and policymakers.  

---

## ▶️ Run the Notebook  
1. Clone repo / upload notebook to Colab  
2. Download dataset:  
   ```bash
   kaggle datasets download -d apollo2506/eurosat-dataset -p data/
   unzip data/eurosat-dataset.zip -d data/eurosat
