Name: Kithusan Albert
Student ID: 8000303 
Course: COMP647 - Machine Learning and Applications 

##  Overview
As part of the COMP647 course, this repository explores a dataset of network session data demonstrating the understanding of application of machine learning fundamentals to a real-world problem.

The course focus on real world problem solving using different types of machine learning algorithms for industrial domains. Identification of inherent characteristics and features of data to obtain hidden patterns and knowledge discovery to understand complex systems.

The EDA analysis explores the dataset of network session data to answer the primary question: "What behaviors or network characteristics are most indicative of a potential cyberattack?". The EDA is structured around two main perspectives:

1.  The Users Behavior: Focuses on actions and attributes related to the user, such as login attempts and IP reputation.
2.  The Network Security: Focuses on the technical characteristics of the network traffic, such as protocol type and encryption.

Kaggle dataset: https://www.kaggle.com/datasets/mmih78367/intrusion-detection

## Network Intrusion Detection Notebook Structure

1.  **Data Preprocessing and Cleaning**
    * 1.1. Handle Duplicates
    * 1.2. Handle Irrelevant Data
    * 1.3. Handle Missing Values
    * 1.4. Handle Outliers
2.  **Exploratory Data Analysis (EDA)**
    * 2.1. EDA: User Behavior
    * 2.2. EDA: Session Network
    * 2.3. EDA Conclusion
3.  **Feature Engineering and Project Re-evaluation**
    * 3.1. New Features
    * 3.2. Data Splitting (Train/Test Split)
    * 3.3. Class Balance
    * 3.4. One-Hot Encoding of Categorical Columns
    * 3.5. Numerical Scaling
4.  **Feature Selection**
    * 4.1. Feature Selection for Supervised Learning Baseline
        * 4.1.1. ANOVA Results
        * 4.1.2. Chi-square Results
        * 4.1.3. RandomForestClassifier Results
    * 4.2. Feature Selection for Unsupervised Anomaly Detection
5.  **Learning (Modeling)**
    * 5.1. Supervised Learning
        * 5.1.1. Logistic Regression Performance
        * 5.1.2. Gradient Boosting Classifier Performance
        * 5.1.3. Linear Support Vector Classifier Performance
        * 5.1.4. Overfitting/Underfitting Analysis
    * 5.2. Unsupervised Learning
        * 5.2.1. Isolation Forest Performance
    * 5.3. Model Performance & Cost-Sensitive Analysis
        * 5.3.1. Comparison: Supervised (Gradient Boosting) vs. Unsupervised (Isolation Forest)
        * 5.3.2. Cost-Sensitive Weight Analysis: Impact on Recall, Precision, F1
        * 5.3.3. Cost-Sensitive Gradient Boosting Classifier Analysis
        * 5.3.4. Cost-Sensitive Gradient Boosting Overfitting/Underfitting Curve
6.  **Explainable AI (XAI)**
    * 6.1. SHAP (SHapley Additive exPlanations)
        * 6.1.1. SHAP Analysis
        * 6.1.2. Unsupervised SHAP Analysis
    * 6.2. LIME (Local Interpretable Model-agnostic Explanations)
        * 6.2.1. LIME Analysis
    * 6.3. t-SNE Insights
7.  **Project Summary**

## Key Findings & Conclusion
- The model analysis (eXplainable AI - XAI) confirmed few behavior metrics were the strongest indicators of an attack. ip_reputation_score and failed_logins were consistently ranked as the most important features by the models.

- Chosen baseline supervised model achieved high accuracy but produced an unacceptably high number of False Negatives (208 missed attacks) which is in a security context is a high risk. 

- Applying a cost-sensitive weight to the Gradient Boosting Classifier model. I was able to reduce assemtrica cost of error and optimized for this security problem. This tuning reduced False Negatives from 208 to 96 while maintaining a high F1-Score of 86%.

- The chosen Gradient Boosting Classifier model (cost-sensitive) model provides the best balance between detecting real threats (high Recall),  maintaining operational practicality (manageable Precision) and aligning with real-world security priorities.

## How to Run

### Create a new conda environment (with Python 3.10)
conda create -n ml_cyber_env python=3.10

### Activate the environment
conda activate ml_cyber_env

### Install the required packages
pip install -r requirements.txt

### Install ipykernel if needed
conda install ipykernel

