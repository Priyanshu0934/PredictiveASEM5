# PredictiveASEM5
dataset Link : https://research.unsw.edu.au/projects/unsw-nb15-dataset 

Network Intrusion Detection Analysis
Project Overview

This project focuses on analyzing and detecting network intrusions using machine learning techniques. With the rapid growth of internet usage, networks are increasingly exposed to cyberattacks such as DoS, exploits, reconnaissance, and malware-based intrusions. An effective Intrusion Detection System (IDS) is essential to identify malicious network traffic and protect systems from potential threats.

In this project, the UNSW-NB15 dataset is used, which contains real-world network traffic with both normal and attack behaviors. The goal is to build and evaluate machine learning models that can accurately distinguish between normal traffic and attacks, and further classify different types of attacks.

Dataset Description

The UNSW-NB15 dataset consists of network flow records generated in a controlled environment. Each record represents a network connection and includes features related to packet counts, byte transfer, timing, protocol behavior, and connection statistics.

The dataset provides:

Normal traffic

Multiple attack categories such as DoS, Exploits, Fuzzers, Reconnaissance, Backdoor, Shellcode, and Worms

Two target columns are used:

label: Binary indicator (0 = Normal, 1 = Attack)

attack_cat: Multiclass label representing the specific attack type

Problem Statement

The objective of this project is to:

Detect whether a network connection is normal or malicious

Identify the type of attack for malicious traffic

This is achieved using supervised machine learning models trained on labeled network traffic data.

Methodology

The project follows a structured machine learning pipeline:

Data Loading and Exploration

Dataset loaded and inspected using shape, info, and null value analysis.

Preprocessing

Categorical features (protocol, service, state) encoded using label encoding.

Original dataset preserved by working on copies.

Binary Classification (Stage 1)

Logistic Regression used to classify traffic as Normal or Attack using the label column.

Multiclass Classification (Stage 2)

Random Forest and SVM models used to classify the type of attack using attack_cat.

Model Evaluation

Models evaluated using accuracy, precision, recall, F1-score, and confusion matrix.

Machine Learning Models Used

Logistic Regression
Used for fast and efficient binary classification (Normal vs Attack).

Random Forest Classifier
Used for multiclass attack classification. Performs well on complex and nonlinear patterns and provides strong overall accuracy.

Support Vector Machine (SVM)
Applied for comparison. Linear and kernel-based SVMs were evaluated, highlighting performance and computational trade-offs.

Results Summary

Logistic Regression achieved strong attack detection with high recall for malicious traffic.

Random Forest produced the best overall performance for multiclass attack classification.

SVM showed limitations on large datasets due to high computational cost and sensitivity to class imbalance.

Conclusion

This project demonstrates how machine learning can be effectively applied to network intrusion detection. A two-stage approach improves efficiency by first detecting attacks and then classifying their types. The results highlight Random Forest as a strong model for complex network traffic analysis, while Logistic Regression serves as a reliable baseline for attack detection.

