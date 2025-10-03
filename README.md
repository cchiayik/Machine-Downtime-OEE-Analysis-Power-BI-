#  Machine Downtime & OEE Analysis (Power BI)

##  Project Overview  
This project leverages **Power BI** to analyze **machine downtime, equipment effectiveness, and failure mechanisms** using the **AI4I 2020 Predictive Maintenance Dataset**.  

The dashboard provides insights into **Overall Equipment Effectiveness (OEE)**, machine failure patterns, risk levels, and key drivers influencing machine breakdowns. It also includes actionable recommendations for **predictive and preventive maintenance**.

##  Dashboard Preview  


### Dashboard for Failure Type Distribution
<img width="1220" height="706" alt="Dashboard for Failure Type Distribution" src="https://github.com/user-attachments/assets/44d15284-339d-4cfa-ba19-835f6e897358"/>
<p align="center"><em>Figure 1: Dashboard showing the distribution of different failure types.</em></p>

### Conditional Formatting based on Tool Wear and Key Influencer
<img width="1244" height="716" alt="Conditional Formatting based on Tool Wear and Key Influencer" src="https://github.com/user-attachments/assets/18bccde9-b5d7-4d1c-b05f-0ac4f5761c2c" />
<p align="center"><em>Figure 2: Conditional formatting applied to highlight tool wear and key influencers.</em></p>

## 📁 Project Structure

- `Impurity_Analysis_Case_Study.ipynb` — Main Python notebook using `pandas`, `statsmodels`, and `matplotlib`
- `Machine DownTime OEE.pdf` — **PDF version** of the dashboard(viewable [here](./Machine DownTime OEE.pdf/))
- `ai4i2020.csv` — Cleaned dataset containing milling machine status and type of failure (viewable [here](./ai4i2020.csv))
- `Impurity_Analysis_Case_Study.pbix` — Dashboard visualizing trends and interactions across variables (download [here](https://github.com/cchiayik/Impurity-Analysis-Case-Study/raw/refs/heads/impurity-analysis-case-study/power_bi/Impurity%20Analysis%20Case%20Study.pbix))

---


## 📂 Dataset  
- **Source:** [`ai4i2020.csv`](./ai4i2020.csv)  
- **Records:** 10,000 product runs  
- **Key Attributes:**
  - `Product ID`, `Type` (L, M, H)  
  - `Tool wear [min]`  
  - `Rotational speed [rpm]`  
  - `Torque [Nm]`  
  - `Temperature differences`  
  - `Machine failure` (binary outcome)  
  - Failure categories:  
    - **TWF** (Tool Wear Failure)  
    - **HDF** (Heat Dissipation Failure)  
    - **PWF** (Power Failure)  
    - **OSF** (Overstrain Failure)  
    - **RNF** (Random Failure)  

---

## 📊 Dashboard Highlights  

###  OEE & Performance Metrics  
- **Overall Failure Rate:** 3.39%  
- **MTBF (Mean Time Between Failures):** 29.5 mins  
- **Availability Rate:** 97%  

###  Failure Type Distribution  
- **HDF (Heat Dissipation Failure):** 30.83%  
- **OSF (Overstrain Failure):** 26.27%  
- **PWF (Power Failure):** 25.47%  
- **TWF (Tool Wear Failure):** 12.33%  
- **RNF (Random Failure):** 5.09%  

###  Key Influencers of Machine Failure  
- **Tool Wear × Torque > 11,919 min·Nm**  
- **Torque > 64.9 Nm** or **< 13 Nm**  
- **Rotational Speed > 2,465 rpm**  
- **Temperature Difference ≤ 8.6 K**  

###  Failure Mechanism (Cascade Effect)  
Excessive tool wear → Reduced cutting efficiency → Increased torque demand → Higher temperature → Heat dissipation failures → Cascading failures  

---

##  Recommendations  

### **Immediate (Next 24h)**  
- Shutdown machines with **Tool Wear > 200 min**  
- Replace tools on **critical risk machines**  
- Adjust operating parameters for borderline machines  

### **Short-term (Next Week)**  
- Implement **predictive maintenance** at 180 min tool wear  
- Retrain operators on torque & RPM safe ranges  
- Install **temperature monitoring alerts** (<8.6 K)  

### **Long-term**  
- Preventive maintenance at **150 min tool wear**  
- Optimize operating parameters within **3,566–8,990 W power range**  
- Upgrade cooling systems for improved **heat dissipation**  

---


