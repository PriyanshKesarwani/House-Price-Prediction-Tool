# 🏢 Indian House Price Prediction System

An interactive machine learning web application that estimates residential real estate prices based on property area, location, room counts, and amenities. Built with **Python**, **XGBoost**, and **Streamlit**.

---

## 📌 Project Overview

Predicting property prices manually is difficult due to wide variations across neighborhoods, unit sizes, and amenities. This project automates the valuation process by:
- Ingesting and cleaning raw real estate data from the Bengaluru Housing Dataset.
- Cleaning square footage anomalies and removing price-per-square-foot outliers.
- Training an **XGBRegressor** model to predict market values.
- Providing a web-based user interface using **Streamlit** for real-time predictions.

---

## ✨ Key Features

- **Automated Data Preprocessing:** Cleans missing values, standardizes fractional square foot ranges, and removes illogical BHK-to-area ratios[cite: 2].
- **Outlier Removal:** Applies statistical standard deviation filtering on price-per-square-foot metrics across individual localities[cite: 2].
- **Dynamic Feature Inputs:**
  - Target neighborhood selection (filtered to locations with high sample density)[cite: 2].
  - Total area (sq ft), BHK count, and bathroom sliders[cite: 2].
  - Property age and essential amenities (swimming pool, gym, 24/7 power backup, gated security)[cite: 2].
- **Dual Currency Output:** Displays estimates automatically in **Lakhs** or **Crores** depending on the valuation bracket[cite: 2].
- **Sidebar Model Diagnostics:** Displays live evaluation metrics ($R^2$ accuracy score and Mean Absolute Error)[cite: 2].

---

## 🛠️ Tech Stack

- **Language:** Python[cite: 2]
- **Machine Learning:** XGBoost (`XGBRegressor`), Scikit-learn[cite: 2]
- **Data Manipulation:** Pandas, NumPy[cite: 2]
- **Web Framework:** Streamlit[cite: 2]
- **Deployment & Tunnelling:** LocalTunnel (for Google Colab deployment)[cite: 2]

---

## 🚀 How to Run the Project

### Option A: Run Locally on Your Computer

1. **Clone the repository:**
   ```bash
   https://github.com/PriyanshKesarwani/House-Price-Prediction-Tool/blob/main/House_Price_Prediction_live.ipynb
1.Install required dependencies:
Bash
pip install streamlit pandas numpy xgboost scikit-learn

2.Launch the application:
Bash
streamlit run app.py
3.Open http://localhost:8501 in your browser to interact with the model[cite: 2].

Option B: Run in Google Colab
If running the notebook in Google Colab:

Run the dependency setup cell:

Bash
!pip install streamlit -q
!npm install -g localtunnel
[cite: 2]

Retrieve your Colab public tunnel IP:

Bash
!wget -qO- ipv4.icanhazip.com
[cite: 2]

Start the application with LocalTunnel:

Bash
!streamlit run app.py & npx localtunnel --port 8501
[cite: 2]

Click the generated loca.lt URL, paste the IP address from Step 2 into the prompt, and submit to access the app[cite: 2].
