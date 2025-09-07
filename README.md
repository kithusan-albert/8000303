
##  Overview
As part of the COMP647 course the repository explores a dataset of network session data. The goal of this project is to understand fundemnetials of Machine learning such as Data Preprocessing and Exploratory Data Analysis (EDA) and machine learning models

The analysis explores a dataset of network session data to answer the primary question: "What behaviors or network characteristics are most indicative of a potential cyberattack?". The EDA is structured around two main perspectives:
1.  The Users Behavior: Focuses on actions and attributes related to the user, such as login attempts and IP reputation.
2.  The Network Security: Focuses on the technical characteristics of the network traffic, such as protocol type and encryption.

## How to Run

General Conda Commands
conda create -n <env_name> python=<python_version>
conda env list : list all environments
conda activate <env_name> : activate respective environment
conda list : list installed libraries
conda install ipykernel : to run jupyter notebook cells. enable kernel

Basic Libraries
conda install pandas
conda install matplotlib
conda install seaborn

Requirements.txt
pip install -r .\requirements.txt
