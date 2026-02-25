# cybersecurity-log-anomaly-detection

## Project Overview
**End-to-End Machine Learning Pipeline for Security Log Analysis**

This project demonstrates a complete data science workflow for detecting anomalies in cybersecurity log data. Designed for Data Science and ML Engineering internship applications, this portfolio piece showcases practical skills in data preprocessing, feature engineering, dimensionality reduction, and unsupervised anomaly detection.

---

## Technical Stack

| Category | Technologies Used |
|----------|-------------------|
| Languages | Python 3.x |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn (DBSCAN, PCA, t-SNE, StandardScaler) |
| Development | Jupyter Notebook |

---

## Project Pipeline

### Step 1: Data Understanding & Cleaning
*Performed comprehensive exploratory data analysis (EDA) on 40,000 security log entries*

**Key Actions:**
- Loaded and inspected dataset structure (25 columns, 40,000 rows)
- Identified data types and missing value patterns
- Dropped low-value columns with approximately 50% nulls and single unique values
- Imputed remaining missing values using mode and median strategies
- Engineered temporal features (`hour`, `day`, `is_nighttime`) from timestamps
- Final shape: 40,000 rows with 25 cleaned features

---

### Step 2: Feature Engineering
*Transformed raw log data into ML-ready features using industry-standard techniques*

**Feature Engineering Highlights:**
- Frequency encoding applied to categorical columns (Protocol, Traffic Type, etc.)
- IP address hashing to convert source and destination IPs to numerical hashes
- Binary encoding for binary categorical features
- Standardization of numerical features using StandardScaler
- Final feature set: 32 engineered features for modeling

---

### Step 3: Dimensionality Reduction
*Visualized high-dimensional data to identify natural attack pattern clusters*

**Techniques Applied:**
- PCA (Principal Component Analysis) to reduce dimensionality while preserving variance
- t-SNE for 2D visualization on a 3000-sample subset
- Key insight: t-SNE plot revealed distinct clustering patterns across different attack types, confirming feature engineering effectiveness

---

### Step 4: Unsupervised Anomaly Detection
*Implemented DBSCAN clustering to identify potential security threats*

**Modeling Approach:**
- Algorithm: DBSCAN (Density-Based Spatial Clustering)
- Objective: Identify outliers and anomalies in feature space
- Implementation:
  - Trained on all 32 numerical features
  - Points labeled as -1 flagged as anomalies
  - Added DBSCAN_Anomaly column to dataset

**Results Visualization:**
- t-SNE plot colored by anomaly labels
- Anomalies appear as scattered points outside main clusters
- Successfully identified potential security threats in unsupervised manner

---

## Key Outcomes and Skills Demonstrated

| Skill Area | Demonstrated Competencies |
|------------|--------------------------|
| Data Wrangling | Missing value handling, data type management, duplicate removal |
| Feature Engineering | Frequency encoding, hashing, temporal feature extraction, standardization |
| Visualization | Correlation heatmaps, distribution plots, t-SNE visualizations |
| ML Modeling | Unsupervised learning with DBSCAN, parameter tuning, anomaly detection |
| Project Structure | End-to-end ML pipeline, reproducible notebook, clear documentation |

---

## Future Enhancements

- Implement additional anomaly detection algorithms (Isolation Forest, One-Class SVM)
- Develop supervised models using labeled attack data
- Create real-time anomaly detection pipeline
- Build interactive dashboard for security analysts

---

## Contact and Links

For any queries or suggestions, please open an issue in the GitHub repository

---

*This project is part of my portfolio for Data Science and Machine Learning internship applications. I am passionate about applying machine learning to cybersecurity challenges and building production-ready data solutions.*
