# DML-with-Categorical-Treatment
This repository accompanies the analysis conducted in "Horizontal Stratification of Higher Education and Gender Earnings Gap in the Early Labor Market".

The study explores how horizontal stratification in higher education, defined by college selectivity and field of study, influences gender wage gaps in the early labor market. The methodology employs Debiased Machine Learning (DML), a robust causal inference framework, extended to settings involving multiple categorical treatments.

A pre-print of the paper is available on SocArXiv: https://osf.io/preprints/socarxiv/kmvse

# Contents of This Repository

This repository contains:

### 1. R Markdown File (`DML_with_Categorical_Treatments.Rmd`):  

A detailed explanation of the DML framework applied to categorical treatments.

- The mathematical foundations of doubly robust estimation.
- The process of extending the DML framework to three treatment categories.
- Annotated R code for implementation.

### 2. PDF File (`DML_with_Categorical_Treatments.pdf`):

A rendered document summarizing the methodology, including:

- Key equations and theoretical explanations.
- R code snippets with step-by-step instructions.

### 3. Sample Dataset (`GOMS.txt`):

A simplified example dataset containing 740 observations.

- Purpose: Since the full dataset used in the study is confidential and too large for practical use in this demonstration, this sample dataset has been created to match the purpose of illustrating the equations and R code.
- Structure: The dataset includes relevant variables, such as covariates and treatment assignments, used in the R Markdown examples.

# Repository Purpose
The purpose of this repository is to provide a detailed demonstration of the DML framework with categorical treatments and to offer a simplified example dataset to help users understand the methodology and replicate the example code.


## 1. Doubly Robust Score Function
$$
\psi(W; \theta, \eta) = \left( Y - g(X) \right) \cdot \left( D - m(X) \right)
$$

### 2. DML Estimator
$$
\hat{\theta} = \frac{1}{n}\sum_{i=1}^n \psi(W_i; \hat{\eta})
$$

### 3. Extension to Multiple Treatments
For \( T \in \{1,2,3\} \):
$$
\hat{\theta}_t = \frac{1}{n}\sum_{i=1}^n \left[ \frac{\mathbb{1}(T_i=t)(Y_i - \hat{g}_t(X_i))}{\hat{p}_t(X_i)} + \hat{g}_t(X_i) \right]
$$

---



# Note on Data Confidentiality
The data used in the published study are confidential and cannot be shared. The materials provided here, including the example dataset, are not replication materials but are intended to illustrate the methodology and implementation.

# Citation
Hwang, Inchan. Horizontal Stratification of Higher Education and Gender Earnings Gap in the Early Labor Market. SocArXiv. DOI: https://osf.io/preprints/socarxiv/kmvse

# Contact
For questions or collaboration inquiries, please contact:
# Inchan Hwang
Email: inchan@yonsei.ac.kr
