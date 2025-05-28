# Cloud Classification from Sentinel-2 using Random Forest

## Overview
This project uses Sentinel-2 surface reflectance imagery to classify cloud coverage using a Random Forest classifier in Google Colab. Labels are simulated using brightness thresholds in visible bands.

## Workflow
1. Export Sentinel-2 data (B2, B3, B4, B8, QA60) from Google Earth Engine.
2. Simulate labels using visible brightness.
3. Train Random Forest on selected bands.
4. Evaluate model (accuracy, confusion matrix, feature importance).
5. Predict and visualize full-scene cloud mask.

## Tools
- Google Colab
- Rasterio
- Scikit-learn
- Matplotlib

## Results
- Accuracy: (see classification report in notebook)
- Most important band: Green
- Cloud mask and RGB image generated

## 🔍 Sample Outputs

### 🌤️ Predicted Cloud Mask
![Predicted Cloud Mask](Predicted%20Cloud%20Mask.png)

### 🖼️ Sentinel-2 RGB Image
![RGB Image](RGB%20Image.png)

### 📉 Confusion Matrix
![Confusion Matrix](Confusion%20Matrix.png)

### 📊 Feature Importances
![Feature Importances](Feature%20Importances.png)

> The model relied most heavily on the Green and Blue bands, consistent with cloud reflectance patterns in the visible spectrum.

## Environmental Cost
This project was executed on CPU using ~170,000 pixels. Model training was under 10 seconds. Estimated CO₂ footprint is negligible (<0.001 kg CO₂). No GPU or large-scale training was required.

## File List
- `cloud_classification_project.ipynb`: Full code
- `Predicted Cloud Mask.png`: Final prediction
- `RGB Image.png`: Sentinel-2 RGB visualization
- `Confusion Matrix.png`: Evaluation of classification
- `Feature Importances.png`: Random Forest band sensitivity
