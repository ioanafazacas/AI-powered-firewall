# AI-powered-firewall
# Network Intrusion Detection System (NIDS) using Machine Learning

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-ML%20Pipeline-orange)](https://scikit-learn.org/)
[![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)]()

This repository contains a **Network Intrusion Detection System (NIDS)** built with **Machine Learning** to identify cyber attacks in network traffic.  
The project is currently under development — the model is trained to detect **DDoS (Distributed Denial of Service)** attacks, and future work aims to extend detection to other types of intrusions such as **PortScan, Web Attacks, and Infiltration**.

---

## 🚧 Project Status

> ⚙️ **Current Phase:** Working prototype  
> ✅ Detects DDoS attacks  
> 🔄 Future Goals: Extend detection to multiple attack types  
> 🧮 Feature extraction performed using **CICFlowMeter** from raw network traffic captures (.pcap files)

---

## 🚀 Overview

This project implements an intelligent NIDS capable of monitoring live or recorded network traffic.  
It uses a **Machine Learning pipeline** to analyze flow-based features and classify each connection as **Normal** or **Intrusion**.

### 🔍 Current Features
- 🧩 Trained ML pipeline (`StandardScaler` + `RandomForestClassifier`)
- ⚙️ Real-time classification of incoming network flows
- 💾 Model persistence with `joblib`
- 📊 Automated output of predictions in CSV format
- 🧮 Features extracted using **CICFlowMeter**

---

### 📁 Repository Structure
├── model_pipeline.joblib # Trained ML pipeline (scaler + classifier)

├── features_used_joblib.joblib # List of features used during training

├── train_model.py # Model training script

├── predict_realtime.py # Real-time prediction script

├── predictions.csv # Generated predictions

├── Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv # Example input dataset

├── requirements.txt # Python dependencies

└── README.md # Project documentation

---
### 🧮 Feature Extraction with CICFlowMeter

All network traffic features were extracted using CICFlowMeter, a tool developed by the Canadian Institute for Cybersecurity.
It converts raw network packets (.pcap files) into flow-based CSV files containing metrics such as:

- Flow duration
- Total forward/backward packets
- Packet length statistics
- TCP flag counts
- Flow IAT (Inter-Arrival Time) metrics
- Active/Idle times
- Average segment sizes

---
### 📊 Dataset

The project uses data derived from the CICIDS2017 dataset, which includes labeled network traffic representing both benign and malicious activities.

Dataset link:
🔗 https://www.unb.ca/cic/datasets/ids-2017.html

