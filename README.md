# PCA: Atmospheric Variables in Bengaluru (2019)

## Overview

Atmospheric datasets often contain multiple interrelated variables such as temperature, humidity, solar radiation, wind speed, and pressure. These variables frequently exhibit multicollinearity, making analysis and interpretation challenging.

This project applies Principal Component Analysis (PCA) to atmospheric data from Bengaluru (2019) to reduce dimensionality, identify underlying environmental factors, and simplify complex weather data while retaining most of the original information.

---

## Objectives

* Analyze relationships among atmospheric variables.
* Reduce dimensionality using Principal Component Analysis.
* Identify the most influential environmental factors affecting weather patterns.
* Evaluate how much information can be retained using a smaller number of components.
* Demonstrate the application of PCA in environmental and climate data analysis.

---

## Dataset Description

### Location

Bengaluru, India

### Year

2019

### Observations

Approximately 2,000 records

### Variables

The dataset contains atmospheric and meteorological variables including:

* Temperature
* Humidity
* Dew Point
* Wind Speed
* Wind Direction
* Atmospheric Pressure
* Global Horizontal Irradiance (GHI)
* Direct Normal Irradiance (DNI)
* Diffuse Horizontal Irradiance (DHI)
* Aerosol Optical Depth
* Additional environmental indicators

After preprocessing, 19 variables were retained for analysis.

---

## Methodology

### 1. Data Cleaning

* Removed irrelevant time-related variables.
* Removed non-informative fields.
* Handled missing values.
* Prepared the dataset for statistical analysis.

### 2. Correlation Analysis

A correlation matrix was generated to examine relationships among variables.

Strong correlations between multiple atmospheric variables indicated the presence of multicollinearity, making PCA an appropriate dimensionality reduction technique.

### 3. KMO Test

The Kaiser-Meyer-Olkin (KMO) Test was performed to assess sampling adequacy.

**Result:** KMO ≈ 0.74

This indicates sufficient shared variance among variables and confirms the suitability of PCA.

### 4. Bartlett's Test of Sphericity

Bartlett's Test was conducted to determine whether variables were significantly correlated.

**Result:** p < 0.05

The null hypothesis was rejected, confirming that PCA could be effectively applied.

### 5. Standardization

Variables were standardized using Z-score normalization to ensure equal contribution regardless of measurement scale.

### 6. Principal Component Analysis

PCA was performed using the covariance matrix approach in R.

Component selection was based on:

* Explained variance
* Scree plot analysis
* Component interpretability

---

## Results

### Variance Explained

| Principal Component | Variance Explained |
| ------------------- | ------------------ |
| PC1                 | 40.7%              |
| PC2                 | 14.8%              |
| PC3                 | 9.1%               |

### Total Variance Explained

The first three principal components explained approximately:

**64.7% of the total variance**

This demonstrates that a relatively small number of components can capture most of the information contained in the original dataset.

---

## Interpretation of Principal Components

### PC1 – Solar Radiation Factor

Major contributors:

* GHI
* DNI
* DHI
* Temperature
* Humidity

Represents overall solar energy intensity and atmospheric radiation conditions.

### PC2 – Atmospheric Moisture Factor

Major contributors:

* Precipitable Water
* Aerosol Optical Depth
* Dew Point

Represents moisture content and atmospheric composition.

### PC3 – Wind & Pressure Dynamics

Major contributors:

* Wind Speed
* Pressure

Represents atmospheric circulation and weather dynamics.

---

## Visualizations

### Scree Plot

The scree plot displays a clear elbow around PC3–PC4, suggesting that 3–4 components are sufficient to represent the dataset effectively.

### PCA Biplot

The biplot illustrates:

* Positive relationships among solar radiation variables.
* Clustering of related atmospheric measurements.
* Opposing directions indicating negative relationships among certain variables.

### PCA Scatter Plot

The PCA scatter plot visualizes how observations are distributed across the first two principal components and highlights the structure of the atmospheric dataset.

---

## Key Findings

* PCA successfully reduced 19 atmospheric variables into a smaller set of meaningful components.
* The first three principal components explained 64.7% of total variance.
* Solar radiation emerged as the dominant environmental factor.
* Atmospheric moisture and wind-pressure dynamics were identified as additional major contributors.
* PCA simplified complex atmospheric data while preserving important information.

---

## Tools & Technologies

* R Programming
* readxl
* psych
* ggplot2
* Principal Component Analysis (PCA)
* Statistical Analysis
* Data Visualization

---

## Repository Contents

```text
├── AS_3.R
├── bengaluru_2019_data.xlsx
├── AS poster final.png
└── README.md
```

---

## Applications

This project demonstrates the use of PCA for:

* Environmental Analytics
* Climate Data Analysis
* Dimensionality Reduction
* Multivariate Statistical Analysis
* Weather Pattern Exploration

---

## Author

**Asmita Baul**

B.Sc. Data Science & Analytics
Jain (Deemed-to-be University)
