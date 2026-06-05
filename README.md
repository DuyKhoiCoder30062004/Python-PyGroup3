# Banking Management Desktop Application

A desktop banking system with AI facial recognition for secure transactions.  
This project was developed as an academic assignment to practice **Fullstack Development** with **Python** and **Tkinter**.

---

## 📌 Project Information
- **Team size:** 4  
- **Role:** Fullstack Developer  
- **Duration:** Feb 2025 – May 2025  
- **Languages/Frameworks:** Python, Tkinter  

---

## 📌 Overview
The system is designed to manage banking operations including customer accounts, transactions, and services.  
It integrates **AI facial recognition** to enhance security for high-value transactions.

---

## 📌 Features
- <mark>Authentication</mark> (login/register)  
- <mark>Main Bank Interface</mark> for account management  
- <mark>Transaction History</mark> tracking  
- <mark>Money Transfer</mark> functionality  
- <mark>Settings</mark> and <mark>Other Services</mark>  
- <mark>AI Facial Recognition</mark> for transactions ≥ 10M VND  

---

## 📌 System Design
- Database schema in <mark>Microsoft SQL Server</mark>  
- Integrated <mark>cv2 Camera</mark> and <mark>Haarcascade</mark> for face detection  
- Built <mark>Training Pipeline</mark> with real face dataset, monitoring overfitting  
- Implemented secure transaction flow with facial recognition  

---

## 📌 AI Training Pipeline
The project integrates an AI facial recognition system to secure high-value transactions.
The training pipeline was designed to process real facial datasets and includes the following steps:

# 1. Data Collection:
 + Gathered a dataset of real face images.
 + Organized into training and validation sets.
# 2. Preprocessing:
 + Applied image resizing and normalization.
 + Used <mark>Haarcascade</mark> for face detection.
 + Augmented data to increase variability.
# 3. Model Training:
 + Built a recognition model using <mark>OpenCV (cv2)</mark>.
 + Trained with supervised learning on facial features.
 + Monitored training and validation accuracy.
# 4. Overfitting Monitoring:
 + Compared training vs validation performance.
 + Identified signs of overfitting (high training accuracy but lower validation accuracy).
 + Adjusted dataset size and preprocessing to mitigate.
# 5. Integration:
 + Connected the trained model with the <mark>Tkinter</mark> banking interface.
 + Facial recognition triggered for transactions ≥ 10M VND.
 + Ensured secure flow before transaction approval.

## 📌 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/DuyKhoiCoder30062004/Python-PyGroup3.git
2. Install required dependencies:
   pip install opencv-python
   pip install pyodbc
3. Configure the SQL Server connection string.
4. Run the application:
   python main.py

## 📌 Screenshots
<div align="center">
<img src="./docs/banking-app.png" width="70%" />
</div>

## 📌 Contribution
Developed by a team of 4 students as part of academic coursework.

##📌 License
This project is for educational purposes only.
