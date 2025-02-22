# 🚀 Big Data Intrusion Detection

## 📌 Project Overview
### **Goal:**  
To build a system that detects cyber attacks in network traffic using **big data processing** and **AI models**.

### **Why Is This Important?**  
- 🔥 **Cyber Attacks Are Increasing** – Organizations need automated intrusion detection.  
- ⏳ **Traditional Security Systems Are Limited** – They can't process large data in real-time.  
- ⚡ **Big Data & AI Improve Detection** – Apache Spark + Machine Learning help analyze huge datasets efficiently.  

---

## 📌 Technologies Used  

| **Technology** | **Purpose** |
|--------------|------------|
| 🛠 **Apache Spark (PySpark)** | Handles large-scale network traffic data efficiently |
| 🔍 **PCA (Principal Component Analysis)** | Reduces dataset size while keeping key patterns |
| 🔄 **ADASYN (Adaptive Synthetic Sampling)** | Balances data by generating synthetic attack samples |
| 🧠 **Machine Learning Models** | Classifies normal vs. attack traffic (Random Forest, Decision Trees, etc.) |
| 🤖 **Deep Learning (LSTM & DDNN)** | Detects complex attack patterns |
| ⚡ **Elephas** | Runs deep learning models on Spark |

---

## 📌 Step-by-Step Explanation  

### **1️⃣ Data Preprocessing & Feature Selection**  
- Uses **network traffic logs** (e.g., **KDD99, NSL-KDD**).  
- Features include:
  - 🏷 **Source/Destination IP, Protocol, Packet Size, etc.**
  - 🔴 **Label (Attack/Normal traffic)**
- **Feature Engineering**: Converts categorical data (e.g., `"protocol type"`) into numbers.  

### **2️⃣ Handling Big Data with Apache Spark**  
- Uses **PySpark** for large-scale processing instead of Pandas.  

### **3️⃣ Dimensionality Reduction with PCA**  
- **Problem**: Too many features make training slow.  
- **Solution**: PCA removes unnecessary features, keeping the key patterns.  

### **4️⃣ Data Balancing with ADASYN**  
- **Problem**: Attack data is rare, making models biased.  
- **Solution**: **ADASYN generates synthetic attack samples** to balance data.  

### **5️⃣ Training Machine Learning Models**  
Trained classifiers:  
✅ **Random Forest**  
✅ **Decision Trees**  
✅ **Logistic Regression**  
✅ **Naïve Bayes**  
✅ **Gradient Boosting**  
📊 **Evaluated using Accuracy, Precision, Recall, and F1-score**.  

### **6️⃣ Training Deep Learning Models**  
- **Deep Dense Neural Network (DDNN)** – Multi-layer neural network.  
- **LSTM (Long Short-Term Memory)** – Detects **patterns over time**.  
- **Trained using Keras + Elephas (Deep Learning on Spark).**  

### **7️⃣ Model Evaluation**  
✅ **Accuracy** – Measures correct predictions.  
✅ **Precision** – Measures how many predicted attacks are real.  
✅ **Recall** – Measures how many actual attacks were detected.  

---

## 🎯 **Final Outcome**
✅ Processes massive network data in **real time**.  
✅ Identifies **normal vs. malicious traffic**.  
✅ Detects **common and rare cyber attacks**.  

---

## 📌 How to Run the Project 🚀  
1. Clone the repository:  
   ```sh
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
