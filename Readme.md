# 🌬️ Wind Turbine Predictive Maintenance & Fault Detection

![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![PowerBI](https://img.shields.io/badge/PowerBI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![ML](https://img.shields.io/badge/Machine%20Learning-Random%20Forest-orange?style=for-the-badge)

## 📌 Executive Summary
This project delivers an enterprise-grade **Predictive Maintenance Solution** designed to minimize unplanned downtime in wind energy farms. By engineering temporal features from SCADA sensor data, the Random Forest model detects underperforming turbines **10-30 minutes in advance** with **96% Precision**.

The insights are operationalized via an interactive **Power BI Command Center**, transforming raw predictions into financial KPIs. This system is projected to save **$1,500 per prevented incident** by enabling proactive rather than reactive maintenance.

---

## 📊 Dashboard Preview
**The "Mission Control" for Site Reliability Engineers.**
![Power BI Dashboard](PowerBI_Dashboard_image.png)
> *The dashboard features a "Traffic Light" risk system, real-time power curve analysis, and a prioritized alert list for technicians.*

---

## 🚀 Key Innovations
### 1. Temporal Feature Engineering ⏳
Standard models often treat sensor readings as isolated events. I engineered **Lag Features** (t-10min, t-20min) and **Rolling Averages** to teach the model "context."
* *Result:* The model understands that a drop in power is only critical if the wind speed has remained high over the last 30 minutes.

### 2. High-Precision AI Model 🧠
* **Algorithm:** Random Forest Classifier (Ensemble Method).
* **Performance:** Achieved **96.1% Accuracy** and **0.98 ROC-AUC**.
* **Reliability:** Drastically reduced False Positives, ensuring technicians are only dispatched for genuine issues.

### 3. Financial ROI Framework 💰
I didn't just predict failures; I quantified them.
* **Cost of Reactive Repair:** ~$2,000
* **Cost of Proactive Maintenance:** ~$500
* **Net Savings:** **$1,500 per incident**.

---

## 🛠️ Tech Stack
| Component | Technologies Used |
| :--- | :--- |
| **Core Logic** | Python, Pandas, NumPy |
| **Machine Learning** | Scikit-Learn (Random Forest), Cross-Validation |
| **Data Viz** | Matplotlib, Seaborn (Static), **Power BI (Interactive)** |
| **Version Control** | Git, GitHub |

---

## 📂 Repository Structure
```text
Wind-Turbine-Predictive-Maintenance/
│
├── data/
│   └── wind_turbine_scada.csv       # Raw sensor data (10-min intervals)
│
├── notebooks/
│   └── 01_data_exploration.ipynb    # Full ML Pipeline (EDA -> Feature Eng -> Modeling)
│
├── outputs/
│   └── final_turbine_predictions.csv # Risk probabilities exported for Power BI
│
├── PowerBI/
│   └── Wind Turbine Dashboard.pbix  # The interactive dashboard file
│
├── requirements.txt                 # Python dependencies
└── README.md                        # Project documentation
