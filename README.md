# ClinicalML: Machine Learning for ICU Outcome Prediction

ClinicalML is a machine learning pipeline designed to predict critical ICU patient outcomes—mortality and length of stay (LoS)—using clinical admission notes from the MIMIC-III dataset. By leveraging Named Entity Recognition (NER), clustering, and traditional ML models, this project demonstrates that lightweight ML approaches can achieve comparable results to transformer-based models while maintaining explainability for clinicians.

## 🚀 Key Features
- **Clinical Outcome Prediction**: Predicts mortality and length of stay using textual data from admission notes.
- **Feature Engineering**: Extracts disease and medication entities using NER (Med7, HunFlair) and applies K-Means clustering on BioClinicalBERT embeddings.
- **ML Models**: Implements traditional models (XGBoost, Logistic Regression, Random Forest) achieving **0.58 F1-score for mortality** and **0.33 F1-score for LoS**.
- **Explainability**: Focuses on interpretable ML models to support clinician decision-making.

## 📁 Repository Structure

### 🔹 Notebooks Overview

| Notebook | Description |
|----------|-------------|
| `MP_using_Doc2vec.ipynb` | Mortality prediction using **Doc2Vec embeddings** from clinical notes. |
| `LOS_using_Doc2vec.ipynb` | Length of stay (LoS) prediction using **Doc2Vec embeddings**. |
| `med_tagger.ipynb` | Extracts **medication-related entities** from clinical notes for drug-based feature engineering. |
| `DRUGS_LOS.ipynb` | Predicts LoS using **drug-based features**, including dimensionality reduction via clustering. |
| `EDA_MIMIC_III_COHORT.ipynb` | Performs **exploratory data analysis (EDA)** on MIMIC-III, summarizing cohort distributions. |
| `Disease_extraction_and_clustering_for_los.ipynb` | Extracts disease mentions using **Flair NER**, clusters disease entities, and analyzes features for LoS prediction. |
| `Mortality_prediction_using_diseases.ipynb` | Mortality prediction based on **disease-related features**. |
| `Mortality_prediction_using_therapeutics.ipynb` | Mortality prediction using **therapeutics (drug-based features)**. |

## 📊 Dataset
- **MIMIC-III v1.4**: A publicly available dataset of de-identified ICU patient records from Beth Israel Deaconess Medical Center.
- The dataset requires credentialed access via [PhysioNet](https://physionet.org/content/mimiciii/1.4/).

## 📌 Results
- **Mortality Prediction (XGBoost, Disease-based Features)**: **0.58 F1-score**
- **Length of Stay Prediction (XGBoost, Disease-based Features)**: **0.33 F1-score**
- Traditional ML models provide competitive performance against transformer-based models while being more interpretable.

---
