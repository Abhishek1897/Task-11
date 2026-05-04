# 📊 Real-Time Log Analysis System

## 📌 Project Overview
This project focuses on building a **real-time log analysis pipeline** to process, analyze, and visualize web server logs. The system leverages modern big data tools to ingest streaming data, process it in real time, and display insights through interactive dashboards.

Log analysis helps in understanding system behavior, identifying issues, improving performance, and enhancing security.

---

## 🚀 Objectives
- Build a real-time data pipeline for log ingestion and processing  
- Analyze NASA web server logs  
- Implement Lambda Architecture (Batch + Speed Layer)  
- Visualize real-time, hourly, and daily insights using dashboards  

---

## 🏗️ Architecture Overview
The system follows a **Lambda Architecture**:

- **Data Ingestion**: Apache NiFi + Apache Kafka  
- **Processing**: Apache Spark Structured Streaming  
- **Storage**:
  - Speed Layer → Cassandra  
  - Batch Layer → HDFS  
- **Visualization**: Plotly + Dash  

👉 The workflow (as shown in the diagram on page 3) includes:
1. Launch EC2 instance  
2. Setup environment via Docker  
3. Ingest dataset  
4. Process streaming data  
5. Visualize insights on Dash  

:contentReference[oaicite:0]{index=0}

---

## 📂 Dataset
- **Source**: NASA Access Logs (Kaggle)  
- **Format**: CSV  
- **Content**:
  - IP address  
  - Timestamp  
  - Request  
  - Status code  
  - Bytes transferred  

---

## 🔄 Data Pipeline Flow
1. **Extraction**
   - Data ingested using Apache NiFi  
   - Logs published to Kafka topics  

2. **Transformation**
   - Schema defined in Spark  
   - Data cleaned and timestamp formatted  

3. **Loading**
   - Real-time data → Cassandra  
   - Batch data → HDFS  

4. **Visualization**
   - Dashboards built using Plotly & Dash  
   - Real-time, hourly, and daily insights  

---

## 🛠️ Tech Stack
- AWS EC2  
- Docker & Docker Compose  
- Apache NiFi  
- Apache Kafka  
- Apache Spark (Structured Streaming)  
- Cassandra  
- HDFS  
- Python  
- Plotly & Dash  

---

## ⚙️ System Requirements
- AWS EC2 instance (recommended: t2.xlarge, 32GB storage)  
- OS: Linux / MacOS / Windows (via PuTTY for EC2 access)  
- Docker installed  

---
📊 Key Features
Real-time log streaming
Scalable pipeline using Kafka & Spark
Dual storage (Cassandra + HDFS)
Interactive dashboards
Supports large-scale log analytics


---
📚 Key Learnings
End-to-end data pipeline design
Streaming data processing
Lambda Architecture implementation
Integration of multiple big data tools
Real-time dashboard development
