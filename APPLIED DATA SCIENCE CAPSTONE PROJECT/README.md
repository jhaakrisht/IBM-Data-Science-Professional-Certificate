# 🚀 Applied Data Science Capstone – Predicting SpaceX Falcon 9 First Stage Landing

## 📄 Summary

This repository showcases the final capstone project from the IBM Data Science Professional Certificate. The objective: to **predict whether the SpaceX Falcon 9 rocket's first stage will land successfully** — a question of both technical precision and profound business impact.

The full analytical journey, from data collection to machine learning model deployment, is meticulously chronicled here. This project exemplifies the confluence of **data science, engineering economics, and predictive analytics** in a real-world aerospace context.

> 📘 *The full report has also been attached as a separate file*

---

## 🧠 Context & Business Understanding

SpaceX has revolutionized space travel by engineering the **reusability of rocket stages** — notably the Falcon 9’s first stage — bringing launch costs down to approximately **$62 million**, compared to the industry norm of **$165 million** or more.

**Being able to predict the success of first-stage landings allows stakeholders to assess the financial viability of a SpaceX launch**, and potentially decide whether to pursue or abstain from competitive bidding.

Thus, this project serves both a **technical function (classification modeling)** and a **strategic purpose (business decision-making)**.

---

## 📑 Project Workflow

### 1. 🛰️ Data Collection
- Acquired launch data using the **SpaceX REST API** via `GET` requests
- Supplemented with **web scraping** from Wikipedia for mission-specific details

### 2. 🧹 Data Wrangling
- Cleaned datasets using `.fillna()` to impute missing values
- Employed `.value_counts()` to:
  - Determine the number of launches by site
  - Identify frequency distributions of orbits and mission outcomes
- Created a **binary landing outcome label**:  
  `1` → successful landing  
  `0` → unsuccessful landing

### 3. 📊 Exploratory Data Analysis
- Queried datasets using **SQL** for structured exploration
- Visualized correlations and distribution patterns using **Pandas** and **Matplotlib**

### 4. 🌍 Interactive Visual Analytics
- Built **geospatial visualizations** using **Folium** to map launch sites and outcomes
- Developed an **interactive dashboard** with **Plotly Dash**, enabling intuitive analysis of launch metrics

### 5. 🧠 Predictive Modeling (Classification)
- Preprocessed data using **StandardScaler**
- Performed **train-test splits** to create robust evaluation protocols
- Trained multiple classifiers, including:
  - Logistic Regression
  - Support Vector Machines
  - Decision Trees
  - K-Nearest Neighbors
- Tuned models using **GridSearchCV**
- Evaluated each model using:
  - **Confusion Matrices**
  - **Accuracy Scores**
  - Other key classification metrics

---

## 🔑 Key Skills Demonstrated

- Applying the **data science lifecycle** to a real-world engineering problem
- Wrangling and analyzing complex datasets for actionable insight
- Developing **interactive dashboards** with **Plotly Dash**
- Conducting **geospatial analysis** using **Folium**
- Building and fine-tuning **machine learning models** for binary classification
- Communicating findings through well-structured reports and visual tools

---

## 📂 Project Artifacts

- Notebooks:
  - `spacex_launch_data_collection.ipynb`
  - `data_wrangling_and_eda.ipynb`
  - `dash_interactive_dashboard.ipynb`
  - `spacex_classifier_models.ipynb`
- Final Dashboard App (`dash_app.py`)
- Supporting Datasets and API Scripts
- Final Report (linked above)

---

## 🧾 Final Thoughts

This capstone project serves as a holistic demonstration of data science in action — an end-to-end pipeline that transforms raw telemetry and mission data into **a decision-support tool** for the aerospace sector.

> “The rocket worked perfectly, except for landing on the wrong planet.”  
> — Wernher von Braun (A reminder for the importance of precision)

