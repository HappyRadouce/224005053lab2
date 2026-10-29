# Lab 2: Anomaly Detection and Cluster Analysis – Country Schools Dataset

## 1. Project Overview

This project focuses on analysing the distribution of digital devices in schools across different counties using data mining and machine learning techniques.

The main purpose is to identify counties with unusual digital device installation patterns and group counties with similar installation characteristics.

The analysis uses the Country Schools Dataset, which contains information about total schools, installed schools, pending schools, installation percentages, Learner Digital Devices (LDDs), and Teacher Digital Devices (TDDs).

## 2. Objectives

The objectives of this lab are to:

- Explore and understand the Country Schools Dataset.
- Clean and preprocess the dataset to prepare it for analysis.
- Identify unusual observations using different anomaly detection techniques.
- Group counties according to their digital device installation patterns.
- Compare different clustering methods.
- Interpret the results and provide recommendations based on the findings.

## 3. Technologies and Libraries Used

The project was implemented using Python and Jupyter Notebook.

The following libraries were used:

- **Pandas:** Data loading, cleaning, and manipulation.
- **NumPy:** Numerical operations.
- **Matplotlib:** Data visualization.
- **Seaborn:** Statistical visualizations.
- **Scikit-learn:** Machine learning and data analysis.
- **SciPy:** Hierarchical clustering and dendrogram visualization.

## 4. Dataset Description

The dataset contains information about schools and digital device distribution across counties.

The main attributes include:

- County
- Total Schools
- Total Schools Installed
- Schools Pending
- Percentage Installed
- Installed Learner Digital Devices (LDDs)
- Installed Teacher Digital Devices (TDDs)

## 5. Methodology

### A. Data Exploration and Preprocessing

The dataset was examined to understand its structure, data types, missing values, and duplicate records.

The following preprocessing activities were performed:

- Removed empty rows and the TOTAL summary row.
- Cleaned and standardised county names.
- Converted installation percentages into numerical values.
- Removed unnecessary identifier columns.
- Corrected numerical data types.
- Removed duplicate records.
- Created a new feature called LDDsPerSchool.
- Standardised selected numerical features using StandardScaler.

Data consistency was also checked to ensure that installed schools and pending schools correctly matched the total number of schools.

### B. Anomaly Detection

Four anomaly detection techniques were applied:

1. **Z-Score:** Identifies observations that are significantly different from the mean.
2. **Interquartile Range (IQR):** Detects outliers using the lower and upper statistical boundaries.
3. **Isolation Forest:** Identifies unusual observations by isolating them from the rest of the dataset.
4. **Local Outlier Factor (LOF):** Detects observations with significantly different local densities.

The results from these techniques were compared to identify counties with unusual digital device installation patterns.

### C. Cluster Analysis

Clustering was performed to group counties with similar characteristics.

The following techniques were used:

- **K-Means Clustering:** Groups counties into three clusters based on their installation profiles.
- **Hierarchical (Agglomerative) Clustering:** Provides another approach to grouping counties and comparing the results.

The Elbow Method and Silhouette Score were used to determine the appropriate number of clusters.

Principal Component Analysis (PCA) was also used to visualise the clusters in two dimensions.

## 6. Key Findings

### Anomaly Detection Findings

The analysis identified several unusual counties:

- **Kitui:** Identified as a positive anomaly because it has a large number of schools and a very high installation rate.
- **Mandera, Wajir, Turkana, and Marsabit:** Identified as counties with low installation rates and unusually high learner devices per installed school.
- **Machakos:** Flagged because of its high number of pending schools.

### Clustering Findings

The K-Means algorithm identified three main county groups:

**Cluster A – Lagging Counties**

Six counties with low installation rates and a high number of learner devices per installed school.

**Cluster B – High Performers**

Twenty-seven counties with relatively high installation rates and fewer pending schools.

**Cluster C – Large Counties in Progress**

Fourteen counties with large numbers of schools, moderate installation rates, and more pending schools.

Hierarchical clustering produced similar groupings, supporting the identified cluster structure.

## 7. Conclusion

The analysis successfully applied anomaly detection and clustering techniques to understand digital device distribution across 47 counties.

The findings revealed differences in school device installation progress, identifying counties with unusually low coverage and others performing well.

The three identified clusters provide a clear understanding of the different installation profiles across counties.

It is recommended that more attention and resources be directed towards lagging counties, while counties with many pending schools should receive support to complete the installation programme.

## 8. Limitations

- The dataset contains only 47 county records.
- Results depend on the selected features and machine learning parameters.
- The dataset does not provide detailed explanations for delays in device installation.

## 9. Project Files

- `notebook.ipynb` – Contains the Python implementation, data preprocessing, anomaly detection, clustering, visualisations, and interpretation of results.
- `README.md` – Provides an overview and documentation of the project.

## 10. Author

**Student Project – Lab 2**

**Coursework:** Anomaly Detection and Cluster Analysis
