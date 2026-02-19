# Assamese-Sentiment-Dataset

## 📌 Overview

This repository contains a curated dataset for **Sentiment Analysis of Assamese Movie Reviews**. The dataset was created and processed as part of a research project focused on applying transfer learning and deep learning techniques to low-resource Indic languages.

The dataset includes both the raw shuffled version and the cleaned, model-ready version, ensuring reproducibility of experiments and transparency in preprocessing.

**NOTE: To get access to the entire artifacts, please refer to my latest GitHub release - Assamese SA**

---

## 📂 Repository Structure

├── Assamese_Movie_Review_Raw_Shuffled.csv
├── Assamese_Movie_Review_Cleaned.csv
└── README.md

---

## 📊 Dataset Details

- **Language:** Assamese (Unicode)  
- **Domain:** Movie Reviews  
- **Total Samples:** 8,987 (1 corrupted entry removed during preprocessing)  
- **Final Usable Samples:** 8,986  

### Sentiment Classes
- Positive  
- Negative  

---

## 📈 Class Distribution

| Sentiment | Count |
|-----------|--------|
| Positive  | 5,677  |
| Negative  | 3,309  |

The dataset has a moderate imbalance (~63% positive, ~37% negative), reflecting natural opinion distribution.

---

## 🗂 Raw Dataset Description

**File:** `Assamese_Movie_Review_Raw_Shuffled.csv`

### Columns:
- `ID` – Unique review identifier  
- `Reviews` – Raw Assamese text  
- `Sentiment` – Label (Positive / Negative)  

The raw dataset contains original collected reviews without aggressive preprocessing.

---

## 🧹 Cleaned Dataset Description

**File:** `Assamese_Movie_Review_Cleaned.csv`

This version is prepared for machine learning experiments.

### Columns:
- `ID`  
- `clean_reviews` – Preprocessed Assamese text  
- `label` – Encoded sentiment (1 = Positive, 0 = Negative)  

---

## 🔍 Preprocessing Steps Applied

The preprocessing was intentionally conservative and linguistically informed:

- Unicode normalization (NFC form)  
- Whitespace normalization  
- Removal of:
  - URLs  
  - HTML tags  
  - Emojis  
  - Special characters  
  - Numbers  
- Punctuation normalization (collapsed repeated punctuation)  
- Stopwords retained (important for Assamese context)  
- No stemming or lemmatization (to preserve subword integrity)  

This ensures compatibility with transformer-based models such as:
- MuRIL  
- IndicBERT  
- XLM-RoBERTa  

---

## 🧠 Research Context

This dataset was used in a comparative study evaluating:

- Transfer Learning Models (MuRIL, IndicBERT, XLM-R)  
- Hybrid Deep Learning (CNN–BiLSTM)  
- Traditional Machine Learning (SVM)  

### Evaluation Metrics Included:
- Accuracy  
- Macro F1-score  
- Macro Precision  
- Macro Recall  
- ROC–AUC  
- Cohen’s Kappa  

The study demonstrates the effectiveness of transfer learning for low-resource Assamese sentiment classification.

---

## ⚙️ Intended Use

This dataset is suitable for:

- Sentiment Analysis research  
- Transformer fine-tuning experiments  
- Low-resource NLP studies  
- Comparative ML vs DL vs Transfer Learning research  
- Assamese language processing research  

---

## 📌 Important Notes

- The dataset is encoded in UTF-8.  
- Assamese text is preserved in Unicode form.  
- Preprocessing is minimal to maintain linguistic integrity.  
- Researchers are encouraged to avoid English-centric preprocessing heuristics.  

---

## 📜 License & Usage

This dataset is released for academic and research purposes.

If you use this dataset in your research, please cite or acknowledge appropriately.

For commercial usage or redistribution, please contact the repository owner.

---

## 👤 Authors

Developed as part of an academic research project on Assamese Sentiment Analysis.

