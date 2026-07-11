# 🥛 Indian Milk Adulteration Detection Dataset

<div align="center">
  
![Dataset](https://img.shields.io/badge/Dataset-CSV-success)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-blue)
![License](https://img.shields.io/badge/License-CC0%201.0-green)
![Python](https://img.shields.io/badge/Python-3.10+-yellow)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

An open-source synthetic dataset designed for machine learning, food safety analytics, anomaly detection, and adulteration classification.

> **Disclaimer:** This dataset is **100% synthetically generated** using statistical simulation informed by FSSAI/BIS standards. It is intended **only for education and research** and must not be used to evaluate or make claims about any real dairy brand.

</div>

---

# 📑 Table of Contents

- Overview
- Dataset Highlights
- Repository Structure
- Files
- Dataset Statistics
- Feature Groups
- Brands Covered
- Adulterant Types
- Machine Learning Tasks
- Quick Start
- Best Practices
- Reference Standards
- Simulation Methodology
- License
- Citation
- Contributing

---

# 📖 Overview

This repository contains a comprehensive synthetic dataset for **Indian milk adulteration detection**. It supports binary classification, multiclass classification, anomaly detection, explainable AI, and educational research.

## 🎯 Applications

- Food Safety
- Machine Learning
- Data Science
- AI Research
- Educational Projects
- Explainable AI
- Feature Engineering

---

# 📊 Dataset Highlights

| Property | Value |
|-----------|------:|
| Samples | 2,500 |
| Brands | 25 |
| Total Columns | 524 |
| Original Features | 128 |
| Metadata Columns | 396 |
| Adulteration Rate | ~5% |
| Adulterant Types | 11 |
| Time Period | Jan 2022–Dec 2023 (Simulated) |
| License | CC0 1.0 |

---

# 📁 Repository Structure

```text
Indian-Milk-Adulteration-Detection-Dataset/
├── milk_combined_full_dataset.csv
├── README.md
├── LICENSE
├── CITATION.cff
```

# 📂 Dataset Files

| File | Description |
|------|-------------|
| milk_combined_full_dataset.csv | Master dataset |
---

# 🧪 Feature Groups

- Sample Identity
- Composition Parameters
- Physical Parameters
- Chemical Tests
- Microbiology
- Enzyme Assays
- Spot Tests
- Fat Quality
- HPLC Protein Profile
- GC-MS Fatty Acid Profile
- NIR Spectroscopy
- Fluorescence Spectroscopy
- Electronic Nose Sensors
- Target Labels

---

# 🏭 Brands Covered

Includes simulated samples for 25 Indian dairy brands including:

- Amul
- Mother Dairy
- Nandini
- Heritage
- Gowardhan
- Milma
- Saras
- Aavin
- Verka
- Country Delight
- Akshayakalpa
- Chitale
- and more.

---

# ⚠️ Adulterants

- Water
- Urea
- Detergent
- Starch
- Formalin
- Hydrogen Peroxide
- Skimmed Milk Powder
- Glucose
- Sodium Bicarbonate
- Vegetable Oil
- Melamine

---

# 🤖 Machine Learning Tasks

## Binary Classification

Target:

```python
Is_Adulterated
```

Recommended models:

- Random Forest
- XGBoost
- CatBoost
- LightGBM
- SVM

## Multiclass Classification

Target:

```python
Adulterant_Detected
```

## Anomaly Detection

Recommended:

- Isolation Forest
- One-Class SVM
- Autoencoder

---

# 🚀 Quick Start

```python
import pandas as pd

df = pd.read_csv("dataset/milk_combined_full_dataset.csv")

print(df.head())
print(df.info())
```

Train a model:

```python
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier

X=df.drop(columns=["Is_Adulterated"])
y=df["Is_Adulterated"]

X_train,X_test,y_train,y_test=train_test_split(
X,y,test_size=0.2,random_state=42,stratify=y)

model=RandomForestClassifier(
n_estimators=200,
class_weight="balanced",
random_state=42)

model.fit(X_train,y_train)
```

---

# ⚠️ Best Practices

- Use F1-score, Recall and ROC-AUC because the dataset is imbalanced.
- Remove metadata columns before training.
- Do not use derived score columns as input features.
- Apply SMOTE only after train/test split.

---

# 📚 Reference Standards

- BIS IS:1479
- FSSAI Food Safety Standards
- ISO 9622
- ISO 11816-1
- AOAC 967.18
- IDF 182

---

# 🔬 Simulation Methodology

The dataset was generated using:

- Truncated normal distributions
- Seasonal variation
- Brand-specific quality profiles
- Physicochemical relationships
- Realistic laboratory sensitivity/specificity
- Domain knowledge from FSSAI and BIS references

---

# 🤝 Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Commit changes.
4. Submit a Pull Request.

---

# 📜 License

Released under **CC0 1.0 Universal**.

---

# 📖 Citation

```text
Om Madav
Indian Milk Adulteration Detection Dataset.
Synthetic Dataset for Machine Learning and Food Safety Research.
Available on Kaggle:
https://www.kaggle.com/datasets/ommadav/indian-milk-adulteration-detection-dataset
```

---

# ⭐ Support

If you find this dataset useful:

- ⭐ Star this repository
- 🍴 Fork it
- 📢 Share it
- 📚 Cite it in your research

---

<div align="center">

Made with ❤️ for the Machine Learning & Food Safety Research Community.

</div>
