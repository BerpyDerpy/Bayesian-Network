# Bayesian Networks


##  **Project Overview: Heart Disease Risk Prediction with Bayesian Networks**

###  **Objective**

- Clean and prepare real-world-inspired health data
-  Construct a Bayesian Network capturing key health dependencies
-  Train the model using Maximum Likelihood Estimation
-  Use probabilistic inference to support diagnostic decision-making


###  **Dataset**

* **File**: `(https://github.com/aiplanethub/Datasets/blob/master/heart_disease.csv)`
* **Key Features Include**:

  * `age`: Patient age
  * `fbs`: Fasting blood sugar indicator
  * `target`: Presence of heart disease (1 = disease, 0 = healthy)
  * `chol`: Cholesterol level
  * `thalach`: Maximum heart rate achieved

###  Project Workflow

**Data Cleaning & Preprocessing**

* Remove duplicate records
* Drop rows with missing values
* Apply Min–Max Normalization to numeric features

**Bayesian Network Construction**

  ```
  age → fbs → target → chol
                      ↘ thalach
  ```
* This captures how age influences blood sugar, which impacts disease risk, further affecting cholesterol and heart function.

**Model Training**

* Use Maximum Likelihood Estimation to compute conditional probability tables from data
* Leverage `pgmpy` for network representation and training

**Inference**

* Estimate disease risk given specific patient characteristics
* Example Queries:

  * Probability of heart disease for a given normalized age
  * Cholesterol distribution for patients with high blood sugar and heart disease

