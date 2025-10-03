# 📊 Machine Downtime & OEE Analysis (Power BI)

## 📌 Project Overview  
This project leverages **Power BI** to analyze **machine downtime, equipment effectiveness, and failure mechanisms** using the **AI4I 2020 Predictive Maintenance Dataset**.  

The dashboard provides insights into **Overall Equipment Effectiveness (OEE)**, machine failure patterns, risk levels, and key drivers influencing machine breakdowns. It also includes actionable recommendations for **predictive and preventive maintenance**.

## 🖼️ Dashboard Preview  
*(Add screenshots of your Power BI dashboard here for visualization.)*  

```markdown
![Dashboard Screenshot 1](images/dashboard1.png)  
![Dashboard Screenshot 2](images/dashboard2.png)  
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

### 🔧 OEE & Performance Metrics  
- **Overall Failure Rate:** 3.39%  
- **MTBF (Mean Time Between Failures):** 29.5 mins  
- **Availability Rate:** 97%  

### ⚠️ Failure Type Distribution  
- **HDF (Heat Dissipation Failure):** 30.83%  
- **OSF (Overstrain Failure):** 26.27%  
- **PWF (Power Failure):** 25.47%  
- **TWF (Tool Wear Failure):** 12.33%  
- **RNF (Random Failure):** 5.09%  

### 📈 Key Influencers of Machine Failure  
- **Tool Wear × Torque > 11,919 min·Nm**  
- **Torque > 64.9 Nm** or **< 13 Nm**  
- **Rotational Speed > 2,465 rpm**  
- **Temperature Difference ≤ 8.6 K**  

### 🛠 Failure Mechanism (Cascade Effect)  
Excessive tool wear → Reduced cutting efficiency → Increased torque demand → Higher temperature → Heat dissipation failures → Cascading failures  

---

## ✅ Recommendations  

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


