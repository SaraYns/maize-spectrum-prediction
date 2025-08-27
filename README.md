# Advanced AI Regression Models for Non-Destructive Prediction of Maize Chemical Composition via Mid-Infrared Spectra Data

This project applies **machine learning models** and **advanced feature selection techniques** to predict maize enzyme activities using **Mid-Infrared (MIR) spectral data**. The goal is to provide a **non-destructive, cost-effective, and accurate alternative** to traditional biochemical analysis.

---

## **Project Overview**
Traditional lab-based analysis of maize chemical composition is time-consuming, costly, and destructive. This project proposes a method using **MIR spectral data + AI models** to predict enzyme activities efficiently.

The workflow includes:
- Spectral **preprocessing** (noise removal, normalization, derivative transformation)
- **Feature selection** (VIP, SPA, CARS, Stepwise, UVE)
- **Regression modeling** (PLSR, LASSO, Ridge, Elastic Net)
- **Model evaluation** using R², RMSE, REP%

---

## **Dataset Description**
The dataset includes:
* **MIR Spectral Data (dataF)**  
  - Absorbance values at 1,868 wavelengths for each maize sample
  - Rows = maize samples, columns = spectral features

* **Enzyme Activity Data (dataC)**  
  - For each sample, five enzyme activities were measured:  
    - **β-glucosidase activity** (nmol g−1 h−1)
    - **N-Acetyl-β-glucosaminidase activity** (nmol g−1 h−1)
    - **Phosphatase activity** (nmol g−1 h−1)
    - **Net peroxidase** (nmol g−1 h−1)
    - **Phenol oxidase** (nmol g−1 h−1)

After cleaning, **258 valid samples** were analyzed.

---

## **Preprocessing**
- **Missing values**: Removed incomplete samples
- **Noise reduction**: Savitzky-Golay smoothing filter
- **Normalization**: Standard Normal Variate (SNV)
- **First derivative transformation**: To enhance subtle peak details

---

## **Feature Selection Methods**
Five feature selection techniques were applied:
1. **VIP (Variable Importance in Projection)** – Based on PLSR, identifies most informative wavelengths
2. **SPA (Successive Projection Algorithm)** – Reduces collinearity, selects non-redundant variables
3. **CARS (Competitive Adaptive Reweighted Sampling)** – Iteratively selects impactful features
4. **Stepwise Regression** – Adds/removes predictors based on statistical significance
5. **UVE (Uninformative Variable Elimination)** – Eliminates low-relevance spectral variables

---

## **Models Implemented**
- **Partial Least Squares Regression (PLSR)**
- **LASSO Regression**
- **Ridge Regression**
- **Elastic Net Regression**

---

## **Evaluation Metrics**
- **R-squared (R²)**
- **Root Mean Square Error (RMSE)**
- **Relative Error of Prediction (REP%)**
- **Cross-validation (k-fold)** for robustness

---

## Project Installation and Setup

### Clone the repository
```
$ git clone https://github.com/SaraYns/maize-spectrum-prediction.git
```
### Navigate to the project directory
```
$ cd maize-spectrum-prediction
```
### Create a virtual environment
```
$ python -m venv .venv
```
### Activate the virtual environment

- **Windows (PowerShell)**
```
$ .venv\Scripts\activate
```
- **Mac/Linux**
```
$ source .venv/bin/activate
```
### Install required Python packages
```
$ pip install -r requirements.txt
```
### Launch Jupyter Notebook
```
$ jupyter notebook
```








