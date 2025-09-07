
##  Overview
As part of the COMP647 course this repository explores a dataset of network session data. The goal of course is to understand fundamentals of machine learning and industry best practices.  

This repository contains a project for the COMP647 course, demonstrating the application of machine learning fundamentals to a real-world cybersecurity problem. The goal is to taught best practices in to a dataset.

The EDA analysis explores the dataset of network session data to answer the primary question: "What behaviors or network characteristics are most indicative of a potential cyberattack?". The EDA is structured around two main perspectives:

1.  The Users Behavior: Focuses on actions and attributes related to the user, such as login attempts and IP reputation.
2.  The Network Security: Focuses on the technical characteristics of the network traffic, such as protocol type and encryption.

Kaggle dataset: https://www.kaggle.com/datasets/mmih78367/intrusion-detection

### How to Run

### Create a new conda environment (with Python 3.10)
conda create -n ml_cyber_env python=3.10

### Activate the environment
conda activate ml_cyber_env

### Install the required packages
pip install -r requirements.txt

### Install ipykernel if needed
conda install ipykernel
