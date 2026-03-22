
# 🧬 Glioma Biomarker Discovery Project

## Multi-Cohort Transcriptomic Integration for Reproducible Biomarker Identification in Glioblastoma and Lower-Grade Glioma

---

## 📌 Overview

This project presents a **multi-cohort transcriptomic analysis framework** for identifying reproducible biomarkers associated with glioma subtype classification and prognosis.

By integrating datasets from:

* **TCGA (UCSC Xena)**
* **CGGA**
* **GEO (GSE16011)**

we identified a robust **21-gene biomarker panel** capable of distinguishing:

👉 **Glioblastoma (GBM)** vs **Lower-Grade Glioma (LGG)**

The analysis includes:

* cross-cohort biomarker discovery
* machine learning model evaluation
* external validation across platforms
* survival analysis
* functional enrichment

---

## 🎯 Key Findings

* Identified **21 reproducible biomarkers** shared across TCGA and CGGA
* Achieved high classification performance:

  * ROC-AUC up to **0.9649 (Random Forest, TCGA)**
  * Cross-validation ROC-AUC ≈ **0.9737**
* External validation (GEO):

  * ROC-AUC = **0.8203**
* Key genes:

  * **TUBA1C, CA9, CLIC1, MMP9, FN1, LOX**
* Functional enrichment highlights:

  * **Extracellular matrix organization**
  * **Collagen formation**
* Strong prognostic signal:

  * TUBA1C associated with poor survival

---

## 🧪 Project Structure

```bash
Glioma_ML_Biomarker_Project/
│
├── data/
│   ├── raw/                  # Original downloaded datasets
│   ├── processed/            # Cleaned and filtered data
│
├── notebooks/
│   ├── 01_data_loading.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_feature_selection.ipynb
│   ├── 04_cgga_validation.ipynb
│   ├── 05_geo_processing.ipynb
│   ├── 06_model_comparison.ipynb
│   ├── 07_tcga_cross_validation.ipynb
│   ├── 08_model_interpretation.ipynb
│   ├── 09_survival_analysis.ipynb
│   ├── 10_functional_enrichment.ipynb
│
├── results/
│   ├── figures/
│   ├── tables/
│
├── README.md
└── requirements.txt
```

---

## ⚙️ Methods Summary

### 1. Data Integration

* TCGA used for discovery
* CGGA used for validation
* GEO used for external cross-platform testing

### 2. Feature Selection

* Random Forest feature importance
* Top 100 genes (TCGA vs CGGA)
* Intersection → **21 shared biomarkers**

### 3. Machine Learning Models

* Logistic Regression
* Random Forest
* XGBoost

### 4. Evaluation

* Train/test split (TCGA)
* 5-fold cross-validation
* External validation (GEO)

### 5. Interpretation

* SHAP for feature importance

### 6. Clinical Analysis

* Kaplan–Meier survival analysis
* Cox proportional hazards model

### 7. Functional Analysis

* GO Biological Process
* KEGG (exploratory)
* Reactome pathways

---

## 📊 Key Results

| Model               | Accuracy | ROC-AUC |
| ------------------- | -------- | ------- |
| Logistic Regression | 0.9098   | 0.9497  |
| Random Forest       | 0.9248   | 0.9649  |
| XGBoost             | 0.9173   | 0.9481  |

**Cross-validation (TCGA):**

* Random Forest ROC-AUC: **0.9737**

**External Validation (GEO):**

* ROC-AUC: **0.8203**

---

## 📈 Visualizations

This project includes:

* ROC curves (TCGA, CGGA, GEO)
* Feature importance plots
* SHAP summary plots
* Expression heatmaps
* Kaplan–Meier survival curves
* Enrichment plots (GO, Reactome)

---

## 🔬 Reproducibility

* All analyses implemented in **Python**
* Random seeds fixed where applicable
* Step-by-step notebooks provided

### Key Libraries

* pandas
* numpy
* scikit-learn
* xgboost
* shap
* lifelines
* gseapy

---

## 📂 Data Sources

* TCGA/Xena: [https://xenabrowser.net](https://xenabrowser.net)
* CGGA: [http://www.cgga.org.cn](http://www.cgga.org.cn)
* GEO (GSE16011): [https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE16011](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE16011)

---

## 🧠 Interpretation

The identified biomarkers are strongly associated with:

* tumor microenvironment remodeling
* extracellular matrix dynamics
* glioma invasiveness

This suggests that the classification model captures biologically meaningful signals linked to disease progression.

---

## 📄 Related Manuscript

**Title:**
*Multi-Cohort Transcriptomic Integration Identifies Reproducible Biomarkers for Glioblastoma–Lower-Grade Glioma Classification and Prognostic Stratification*


---

## 👨‍💻 Author

**Musa Al Hassan Kromah**
MSc Biotechnology | Bioinformatics & Computational Biology

---

## 📜 License

This project is released under the MIT License.

