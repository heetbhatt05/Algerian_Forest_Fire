# 🔥 Algerian Forest Fire Predictor

This is an End-to-End Machine Learning project that predicts the **Fire Weather Index (FWI)** based on weather conditions in Algerian forest regions. The project implements a complete pipeline from Data Cleaning to Model Deployment using **Flask**.

## 📌 Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation & Usage](#installation--usage)
- [Model Information](#model-information)
- [Screenshots](#screenshots)

## 📖 Overview
Forest fires are a major environmental concern. This project analyzes weather data from the Bejaia and Sidi Bel-Abbes regions in Algeria to predict the likelihood of a forest fire. 

The core prediction is the **FWI (Fire Weather Index)**, which is a standard index used to estimate the danger of fire.

## 📂 Dataset
The dataset was obtained from the **UCI Machine Learning Repository**.
- **Regions:** Bejaia (Region 0) and Sidi Bel-Abbes (Region 1).
- **Features:** Temperature, Humidity (RH), Wind Speed (Ws), Rain, FFMC, DMC, DC, ISI, BUI.
- **Target:** FWI (Fire Weather Index).

## 🛠️ Technologies Used
* **Language:** Python 3.x
* **Web Framework:** Flask
* **Machine Learning:** Scikit-Learn (Ridge Regression)
* **Data Processing:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Frontend:** HTML5, CSS3 (Custom Dashboard Design)
* **Serialization:** Joblib

## 📁 Project Structure

```

Algerian_Forest_Fire/
│
├── models/
│   ├── ridge.pkl        # Trained Model
│   └── scaler.pkl       # StandardScaler Object
│
├── templates/
│   └── home.html        # Web Dashboard UI
│
├── 1_EDA_and_Cleaning.ipynb    # Data Analysis & Cleaning Notebook
├── 2_Model_Training.ipynb      # Model Training Notebook
├── app.py                      # Flask Application
├── requirements.txt            # List of dependencies
├── Algerian_forest_fires_dataset_UPDATE.csv # Raw Dataset
└── README.md

```

## ⚙️ Installation & Usage

**1. Clone the Repository**
```bash
git clone [https://github.com/heetbhatt05/Algerian_Forest_Fire.git](https://github.com/heetbhatt05/Algerian_Forest_Fire.git)
cd Algerian_Forest_Fire

```

**2. Create a Virtual Environment (Optional but Recommended)**

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

```

**3. Install Dependencies**

```bash
pip install -r requirements.txt

```

*(Note: If `requirements.txt` is missing, install manually: `pip install flask pandas numpy scikit-learn matplotlib seaborn joblib`)*

**4. Run the Application**

```bash
python app.py

```

**5. Access the Web App**
Open your browser and go to: `http://127.0.0.1:5000/`

## 🧠 Model Information

* **Preprocessing:** Removed "Classes" column to prevent leakage, cleaned whitespace, handled missing values, and encoded regions.
* **Scaling:** Used `StandardScaler` to normalize feature distributions.
* **Algorithm:** `Ridge Regression` was chosen as the best performer (over Linear, Lasso, and ElasticNet) to handle multicollinearity between weather features.
* **Metrics:** Evaluated using R2 Score and MAE (Mean Absolute Error).

## 📸 Screenshots

![Dashboard Screenshot](screenshots/dashboard.png)


**Created by [Heet Bhatt](https://www.google.com/search?q=https://github.com/heetbhatt05)**
