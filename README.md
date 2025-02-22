# Bigdata

Project Overview: Intrusion Detection Using Big Data & Deep Learning
Goal:
To build a system that detects cyber attacks in network traffic using big data processing and AI models.

Why Is This Important?
Cyber Attacks Are Increasing – Organizations need automated intrusion detection.
Traditional Security Systems Are Limited – They can't process large data in real-time.
Big Data & AI Improve Detection – Apache Spark + Machine Learning help analyze huge datasets efficiently.

1. Technologies Used in This Project
The project uses big data, machine learning, and deep learning for intrusion detection:

Technology	Purpose
Apache Spark (PySpark)	Handles large-scale network traffic data efficiently
PCA (Principal Component Analysis)	Reduces dataset size while keeping key patterns
ADASYN (Adaptive Synthetic Sampling)	Balances data by generating synthetic attack samples
Machine Learning Models	Classifies normal vs. attack traffic (Random Forest, Decision Trees, etc.)
Deep Learning (LSTM & DDNN)	Detects complex attack patterns
Elephas	Runs deep learning models on Spark
2. Step-by-Step Explanation of the Project
Step 1: Data Preprocessing & Feature Selection
The dataset likely comes from network traffic logs (e.g., KDD99, NSL-KDD).
It includes features like:
Source/Destination IP, Protocol, Service Type, Packet Size, etc.
Label (Attack/Normal traffic)
Feature Engineering: Converts categorical data (like "protocol type") into numbers.
Step 2: Handling Big Data with Apache Spark
Since network data is huge, Spark (PySpark) is used instead of Pandas.
Spark processes data in parallel, making it much faster.
Step 3: Dimensionality Reduction with PCA
Problem: Too many features make training slow and less accurate.
Solution: PCA removes less important features while keeping useful patterns.
Step 4: Data Balancing with ADASYN
Problem: Attack data is rare, making models biased toward normal traffic.
Solution: ADASYN (Adaptive Synthetic Sampling) generates synthetic attack data to balance classes.
Step 5: Training Machine Learning Models
The following models are trained:
Random Forest
Decision Trees
Logistic Regression
Naïve Bayes
Gradient Boosting
They are evaluated using Accuracy, Precision, Recall, and F1-score.
Step 6: Training Deep Learning Models
Deep Dense Neural Network (DDNN): A multi-layer neural network for classification.
LSTM (Long Short-Term Memory): Detects patterns over time, useful for attacks spread over multiple packets.
These models are trained using Keras + Elephas (which allows deep learning on Spark).
Step 7: Model Evaluation
Models are tested on a separate dataset.
Performance is measured using:
Accuracy (Correct predictions)
Precision (How many predicted attacks are real)
Recall (How many actual attacks were detected)
3. Final Outcome
After training, the project outputs a trained AI model that can: ✅ Process massive network data in real time
✅ Identify normal vs. malicious traffic
✅ Detect both common and rare attack types
