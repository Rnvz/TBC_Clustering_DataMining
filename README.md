# 🧬 Tuberculosis (TBC) Case Distribution Analysis in Jakarta Using Clustering

## 🎯 Project Overview
This project analyzes the **distribution of Tuberculosis (TBC) cases across Jakarta** using the **Agglomerative Hierarchical Clustering** method.  
The objective is to identify **priority intervention areas** and assist the government in formulating **data-driven health policies** for better disease control.

---

## 📊 Dataset
**Sources:**
- Jakarta Provincial Health Office (Dinas Kesehatan DKI Jakarta)  
- Central Bureau of Statistics (BPS Jakarta)  
- Jakarta Open Data Portal (Satu Data Jakarta)  

**Period:** 2020–2023  
**Total records:** 267 sub-districts  

**Main Features:**
- Number of TBC cases  
- Population density  
- Poverty rate  
- Number of hospitals (general & special)  
- Air Pollution Index (ISPU)

---

## ⚙️ Methodology
1. **Data Preprocessing**
   - Combined data from multiple sources (Health Office, BPS, ISPU)
   - Cleaned and filled missing values with 0  
   - Scaled data using `RobustScaler`  
   - Reduced dimensionality with **PCA (2 principal components)**  

2. **Clustering**
   - Model: `Agglomerative Hierarchical Clustering`
   - Parameter: `distance_threshold = 10`
   - Number of clusters formed: **9**
   - **Silhouette Score:** 0.7817 (indicating well-separated clusters)

---

## 🔍 Key Findings
- **Cluster 0:** Majority of sub-districts with moderate TBC cases and limited facilities.  
- **Clusters 5 & 8:** Extreme cases — high prevalence (>500/100,000 population) and no hospital presence.  
- **Clusters 4 & 6:** High TBC rates but low healthcare access.  
- **Joglo (West Jakarta)** identified as a **top intervention priority area**.  

---

## 💡 Insights
- Highly populated areas with poor healthcare access show higher TBC vulnerability.  
- Clustering results can guide **targeted intervention and resource allocation**.  
- The model can be extended for **spatial-based early warning systems** for public health management.

---

## 🧠 Tools & Libraries
- **Python**  
- **Pandas**, **NumPy**  
- **Scikit-learn** (Agglomerative Clustering, PCA, RobustScaler)  
- **Matplotlib**, **Seaborn**

---

## 📚 Data References
- [Jakarta Provincial Health Office Dataset](https://docs.google.com/spreadsheets/d/1UQZU7D7wkznfcLHF3_xHVtuLkdQIvr_496H49UL3sGk)  
- [BPS Jakarta](https://jakarta.bps.go.id)  
- [Satu Data Jakarta](https://satudata.jakarta.go.id)

---

## 🏁 Summary
This study successfully classified Jakarta’s sub-districts into **9 clusters** representing different TBC risk levels.  
The results can help policymakers focus on **critical zones** with high prevalence and limited healthcare infrastructure, ultimately contributing to **more effective public health strategies**.
