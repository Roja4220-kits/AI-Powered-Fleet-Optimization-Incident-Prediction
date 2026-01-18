#  AI-Powered Fleet Optimization & Road Incident Prediction

This repository contains an enterprise-level smart logistics system developed as part of **Task-4 during the internship at Flipkart Pvt Ltd**.  
The project integrates **machine learning, optimization algorithms, real-time data simulation, and geospatial intelligence** to enhance transportation safety and efficiency.

---

##  Project Objectives

- Predict potential road incidents such as accidents, breakdowns, and slowdowns
- Optimize fleet scheduling and vehicle assignment in real time
- Dynamically reroute vehicles during high-risk situations
- Visualize live fleet operations through an interactive dashboard

---

##  System Architecture (High Level)

- Real-Time Data Generator
- Incident Prediction Engine
- Fleet Scheduling Optimization Module
- Dynamic Rerouting System
- Monitoring Dashboard
- Mini MLOps Automation Layer

---

## 📦 Functional Modules

### 1️⃣ Real-Time Data Integration
Simulates continuous streaming data including:
- GPS coordinates
- Vehicle speed and engine health
- Driver behavior metrics
- Traffic and weather conditions
- Historical accident patterns

### 2️⃣ Incident Prediction System
Machine learning models used:
- Random Forest
- XGBoost
- CatBoost
- LSTM / GRU

Predictions include:
- Accident probability
- Vehicle breakdown risk
- Route slowdowns
- Blockage likelihood

### 3️⃣ Fleet Scheduling Optimization
Optimizes vehicle-task assignments considering:
- Distance and travel time
- Vehicle capacity
- Driver shift limits
- Traffic conditions

Optimization techniques:
- Genetic Algorithms
- Simulated Annealing
- Google OR-Tools (VRP)

### 4️⃣ Dynamic Rerouting
- Detects high-risk routes
- Selects safer alternatives
- Updates ETA dynamically
- Logs rerouting events

### 5️⃣ Monitoring Dashboard
- Live GPS tracking
- Incident risk visualization
- Fleet utilization metrics
- Route recommendations
- Driver behavior alerts

---

## 🛠️ Tools & Technologies

- **Programming Language:** Python
- **Data Processing:** pandas, numpy
- **Machine Learning:** scikit-learn, xgboost, catboost, tensorflow
- **Optimization:** Genetic Algorithm, Google OR-Tools
- **Geospatial:** geopy, folium
- **Dashboard:** Streamlit / Dash
- **Streaming (Optional):** Kafka / Python Generators

---

## 📊 Model Evaluation Metrics

- Precision
- Recall
- F1-Score
- ROC-AUC
- False Negative Rate

---

## ⚙️ Automation & MLOps (Mini)

- Periodic model retraining
- Drift detection
- Model versioning
- Prediction confidence logging

---
## **How to Execute the Project (Notebook + Multi-Terminal Execution)**
his project is designed to automatically generate its full folder structure and Python modules by executing a single Jupyter Notebook, followed by running individual system components in parallel terminals.

**Step 1: Create Project Folder in Jupyter**

Open Jupyter Notebook (Anaconda Navigator)

On the Jupyter home page, manually create a new folder named:

AI-Powered-Fleet-Optimization-Incident-Prediction


Open this folder.

**Step 2: Upload and Run the Notebook**

Upload the Jupyter Notebook file available in this repository:

task4.ipynb


Open task4.ipynb

Click Kernel → Restart & Run All

📌 What this does (Important):

Automatically creates all project folders

Generates required Python files

Builds phase-wise modules inside
AI-Powered-Fleet-Optimization-Incident-Prediction/

No manual folder or file creation is required after this step.

**Step 3: Open Anaconda Prompt (Multiple Terminals)**

Open 5 separate Anaconda Prompt terminals (Terminal 1 to Terminal 5).

**🚀 Phase-wise Execution (Parallel Terminals,creates csv files internally and updates continuously)**

**🔹 Terminal 1: Train Incident Prediction Models**

cd AI-Powered-Fleet-Optimization-Incident-Prediction

python phase2_incident_prediction/train_incident_models.py


**(Output):**

Trains Random Forest, XGBoost, CatBoost, and LSTM/GRU models

Saves trained models into the models/ folder

Displays training accuracy and evaluation metrics

**🔹 Terminal 2: Start Real-Time Data Generator**

cd AI-Powered-Fleet-Optimization-Incident-Prediction

python phase1_realtime_stream/data_generator.py


**(Output):**

Simulates live GPS, vehicle health, driver behavior, traffic, and weather data

Continuously streams real-time fleet data

Acts as the data source for live prediction

**🔹 Terminal 3: Run Live Incident Prediction (Inference)**

cd AI-Powered-Fleet-Optimization-Incident-Prediction

python phase1_realtime_stream/phase2_live_inference.py


**(Output):**

Consumes real-time streamed data

Generates live incident risk predictions

Sends prediction results to downstream modules

**🔹 Terminal 4: Execute Fleet Optimization Engine**

cd AI-Powered-Fleet-Optimization-Incident-Prediction

python phase3_fleet_optimization/fleet_optimizer.py


**(Output):**

Optimizes vehicle-to-task assignments

Minimizes fuel cost, delay, and idle time

Produces optimized fleet schedules

**🔹 Terminal 5: Run Dynamic Rerouting System**

cd AI-Powered-Fleet-Optimization-Incident-Prediction

python phase4_dynamic_rerouting/dynamic_rerouting.py


**(Output):**

Detects high-risk routes based on predictions

Automatically reroutes affected vehicles

Updates ETA and logs rerouting events

**🔹 Terminal 6 : Launch Dashboard**

cd AI-Powered-Fleet-Optimization-Incident-Prediction

streamlit run phase5_dashboard/dashboard.py


**(Output):**

Launches interactive dashboard in browser

**Displays:**

Live GPS tracking

Incident risk alerts

Fleet utilization metrics

Dynamic route suggestions

Driver behavior alerts

---


## 🔄 **Execution Flow**

Notebook (Auto File Creation)
        |
        v
Real-Time Data Stream
        |
        v
Incident Prediction
        |
        v
Fleet Optimization
        |
        v
Dynamic Rerouting
        |
        v
Live Monitoring Dashboard


---

⚠️ **Important Notes**

All terminals must run simultaneously for real-time behavior

Ensure all dependencies are installed using requirements.txt

This project uses simulated data for demonstration purposes

