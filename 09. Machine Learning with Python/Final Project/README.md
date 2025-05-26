# 🤖 Machine Learning with Python – The Best Classifier

## 📄 Summary

This project represents the culminating exercise of the "Machine Learning with Python" course under the IBM Data Science Professional Certificate. The primary objective is to construct and evaluate a **predictive classifier** that determines whether a loan applicant is likely to pay off their loan — a quintessential example of binary classification in action.

Through methodical experimentation and rigorous evaluation, this notebook compares multiple algorithms to identify the most performant model for the task at hand.

---

## 📝 Methodology

A historical dataset of past loan applications is ingested and subjected to a meticulous **data preprocessing pipeline**. This includes cleansing, normalization, and transformation into a format amenable to machine learning. The data is then bifurcated into **training and testing subsets** to allow for both model training and out-of-sample evaluation.

### 🧠 Classifiers Trained

Each of the following machine learning algorithms was implemented using **Scikit-learn**, and trained on the processed dataset:

- **k-Nearest Neighbour (k-NN)**
- **Decision Tree**
- **Support Vector Machine (SVM)**
- **Logistic Regression**

### 📊 Evaluation Metrics

To determine the efficacy of each classifier, the following performance indicators were employed:

- **Jaccard Index** – Measures similarity between predicted and actual sets
- **F1-score** – Balances precision and recall, especially valuable for imbalanced data
- **Log Loss** – Applied specifically to **Logistic Regression**, quantifying the uncertainty of predictions

---

## 🔍 Insights

This analytical endeavour showcases the diversity of approaches to solving classification problems and underscores the importance of evaluation metrics tailored to model context and business goals. By juxtaposing algorithmic performance, the notebook surfaces not only the "best" classifier in terms of metrics, but also provides rationale for real-world selection.

> “Prediction is very difficult, especially if it’s about the future.”  
> — Niels Bohr

---

## 📂 Contents

- Jupyter Notebook: `loan_classifier_comparison.ipynb`
- Dataset: Preprocessed loan data (CSV)
- Output report: Accuracy scores and comparative metric analysis

---

## 🧾 Final Thoughts

This project exemplifies the applied dimension of machine learning — transforming historical patterns into actionable foresight. The exercise goes beyond syntax, delving into the interpretability and strategic implications of model choice in the broader ecosystem of decision intelligence.

