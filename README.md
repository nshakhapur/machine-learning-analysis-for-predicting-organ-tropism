# Breast Cancer Metastasis Prediction using Gene Expression Data

This repository contains code and analysis for classifying breast cancer metastasis sites (Bone, Brain, Liver, and Lung) using machine learning models based on gene expression data. It employs Random Forest, Support Vector Machine (SVM), and Neural Networks to identify key genetic markers associated with organ-specific metastasis.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Feature Selection](#feature-selection)
- [Models Used](#models-used)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Contributors](#contributors)
- [License](#license)

---

## Introduction
This project aims to predict the organ-specific metastasis of breast cancer based on gene expression profiles. Using **machine learning and deep learning models**, we attempt to identify the most influential genes that contribute to metastasis and improve classification accuracy.

---

## Dataset
- **Source:** GEO Dataset (GSE14020)
- **Link:** https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE14020
- **Preprocessing:** Data was extracted, normalized, and annotated to map gene IDs to gene symbols.
- **Metastasis Labels:** Four metastasis sites - *Bone, Brain, Liver, and Lung*.

---

## Methodology
1. **Data Preprocessing**:
   - Extract gene expression data.
   - Standardize features.
   - Encode categorical metastasis labels.
   
2. **Feature Selection**:
   - Identify top 20 genes using **Random Forest Feature Importance**.
   - Further refine using **Recursive Feature Elimination (RFE)** and **Lasso Regression**.
   - Select the final 9 most important genes.

3. **Model Training & Evaluation**:
   - Train **Random Forest, SVM, and Neural Networks**.
   - Compare accuracy, precision, recall, and F1-score.
   - Use **Confusion Matrix** and **Radviz plots** for visualization.

---

## Feature Selection
To improve model interpretability and reduce dimensionality, we used:
- **Random Forest Feature Importance** to rank genes by their contribution.
- **Recursive Feature Elimination (RFE)** to iteratively remove less important features.
- **Lasso Regression** to further refine the most predictive genes.

---

## Models Used
- **Random Forest Classifier**
- **Support Vector Machine (SVM)**
- **Artificial Neural Network (ANN)**

---

## Results
- **Neural Network achieved the highest accuracy** (*92.3%*) outperforming SVM and Random Forest.
- **CCL19, FABP7, and COL1A2** were found to be the most influential genes in metastasis prediction.
- The **Confusion Matrix and Radviz plot** validated model performance.

---

## Installation
To run this project locally, follow these steps:

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/yourusername/breast-cancer-metastasis.git
   cd breast-cancer-metastasis
   ```

2. **Install Dependencies**:
   ```sh
   pip install -r requirements.txt
   ```

3. **Run the Main Script**:
   ```sh
   python main.py
   ```

---

## Usage
- Run the scripts to **train models and visualize results**.
- Modify `config.py` to change model parameters.
- Use **Jupyter Notebook (`analysis.ipynb`)** for interactive analysis.

---

## Contributors
Sohini Chakraborty, Nidhi Shakhapur


---

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
