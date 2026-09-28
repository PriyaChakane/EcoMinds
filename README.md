# EcoMinds 🌱

## AI-Powered Environmental Monitoring and Risk Intelligence Platform

EcoMinds is a full-stack environmental intelligence platform designed to monitor environmental conditions, analyze air-quality and sensor data, identify environmental risks, track violations, and provide data-driven insights through an interactive web dashboard.

The platform combines **Flask, Python, machine learning, environmental data processing, sensor integration, risk prediction, and interactive dashboards** to provide a centralized system for environmental monitoring and decision support.

---

## 🚀 Features

### 🌍 Environmental Monitoring

* Monitor environmental and sensor-based parameters
* Process real-time and historical sensor data
* Track environmental conditions through a centralized dashboard
* Support for hardware-based sensor data collection

### 📊 Air Quality Analysis

* Air Quality Index (AQI) calculation
* Environmental parameter analysis
* Sensor data processing and visualization
* Historical environmental data tracking

### 🤖 Machine Learning Risk Prediction

* Machine learning-based environmental risk prediction
* Multi-risk prediction capabilities
* Pre-trained ML models for risk assessment
* Feature-based environmental risk analysis

### 🚨 Violation Detection

* Identify environmental violations
* Process violation-related data
* Track violation details
* Provide dedicated violation dashboards

### 🧠 Environmental Intelligence

* Generate environmental insights
* Analyze environmental patterns
* Provide risk-related information
* Support data-driven environmental decision-making

### 💬 AI Chatbot

* Interactive environmental chatbot
* Provides information through the application interface
* Integrated with the Flask backend

### 📱 Interactive Dashboard

The platform includes dedicated interfaces for:

* Dashboard
* Active Devices
* My Devices
* City Map
* Environmental Intelligence
* Multi-Risk Analysis
* Parameter Monitoring
* Violation Details
* Alert Logs
* Accuracy Monitoring
* Subscription
* User Authentication

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────────┐
                    │       User / Admin      │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │     Web Dashboard       │
                    │ HTML / CSS / JavaScript │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │      Flask Backend      │
                    │          app.py         │
                    └────────────┬────────────┘
                                 │
              ┌──────────────────┼──────────────────┐
              │                  │                  │
              ▼                  ▼                  ▼
       ┌────────────┐     ┌─────────────┐    ┌──────────────┐
       │   Routes   │     │  Services   │    │   Database   │
       └────────────┘     └─────────────┘    └──────────────┘
              │                  │                  │
              │                  ▼                  │
              │          ┌──────────────┐          │
              │          │ ML Prediction│          │
              │          │ Risk Analysis│          │
              │          └──────────────┘          │
              │                  │                  │
              └──────────────────┼──────────────────┘
                                 ▼
                    ┌─────────────────────────┐
                    │ Environmental Insights  │
                    │ Risk & Violation Data   │
                    └─────────────────────────┘
```

---

## 🛠️ Technology Stack

### Backend

* Python
* Flask
* Flask Routes
* REST-style application architecture

### Machine Learning

* Python-based ML models
* Pickle-based trained models
* Feature-based risk prediction
* Multi-risk prediction

### Database

* SQLite
* Database helper utilities
* Alert database
* Environmental data storage

### Frontend

* HTML
* CSS
* JavaScript
* Jinja2 Templates

### Data & Environmental Processing

* Sensor data processing
* AQI calculation
* Environmental parameter analysis
* Risk analysis

### Hardware Integration

* Sensor data collection
* Hardware server
* Sensor-data processing utilities

---

## 📁 Project Structure

```text
EcoMinds/
│
├── app.py
├── config.py
├── backfill_insights.py
├── requirements.txt
│
├── database/
│   ├── __init__.py
│   ├── alert_db.py
│   ├── db_helper.py
│   ├── init_db.py
│   └── seed_dummy_data.py
│
├── Hardware_set_up/
│   ├── cleaned_sensor_data.csv
│   ├── hardware_server.py
│   ├── database_view.py
│   └── name_change.py
│
├── models/
│   ├── README.md
│   ├── multi_risk_features.pkl
│   ├── multi_risk_model.pkl
│   ├── risk_features_list.pkl
│   └── risk_model.pkl
│
├── routes/
│   ├── auth.py
│   ├── active_devices.py
│   ├── chatbot.py
│   ├── citymap.py
│   ├── dashboard.py
│   ├── intelligence.py
│   ├── multirisk.py
│   ├── my_devices.py
│   ├── parameter.py
│   ├── subscribe.py
│   └── violation.py
│
├── services/
│   ├── alert_service.py
│   ├── aqi_calculator.py
│   ├── email_scheduler.py
│   ├── email_service.py
│   ├── multirisk_engine.py
│   ├── recommendation.py
│   ├── risk_predictor.py
│   └── violation_engine.py
│
├── static/
│   ├── css/
│   ├── images/
│   └── js/
│
└── templates/
    ├── dashboard.html
    ├── intelligence.html
    ├── citymap.html
    ├── multirisk.html
    ├── violation_detail.html
    ├── login.html
    ├── register.html
    └── ...
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/PriyaChakane/EcoMinds.git
cd EcoMinds
```

Because the current repository contains nested project directories, enter the actual application directory:

```bash
cd "EcoMind_antiGra (2)new/EcoMind_antiGra (3)/EcoMind_antiGra"
```

### 2. Create a virtual environment

Windows:

```powershell
python -m venv .venv
```

Activate it:

```powershell
.venv\Scripts\activate
```

### 3. Install dependencies

```powershell
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the application directory and add the required configuration values.

**Do not commit `.env` to GitHub.**

### 5. Initialize the database

If required by the application:

```powershell
python database\init_db.py
```

### 6. Run the application

```powershell
python app.py
```

The Flask application will then be available through the local development server.

---

## 🧠 Machine Learning Pipeline

EcoMinds uses trained machine learning models to support environmental risk analysis.

The general workflow is:

```text
Sensor / Environmental Data
            │
            ▼
     Data Processing
            │
            ▼
    Feature Preparation
            │
            ▼
   Machine Learning Model
            │
            ▼
      Risk Prediction
            │
            ▼
 Environmental Intelligence
            │
            ▼
      Dashboard / Alerts
```

The project contains trained model files and corresponding feature definitions inside the `models/` directory.

---

## 🌫️ AQI Processing

The platform includes an AQI calculation service that processes environmental parameters and generates air-quality information.

The resulting information can be used by the application for:

* Air-quality monitoring
* Environmental analysis
* Risk assessment
* Dashboard visualization
* Environmental recommendations

---

## 🚨 Risk & Violation Management

EcoMinds provides services for identifying and managing environmental risks and violations.

The platform includes:

* Risk prediction
* Multi-risk analysis
* Violation detection
* Violation details
* Alert management
* Environmental recommendations

This allows environmental information to be presented in a structured format through the dashboard.

---

## 📡 Hardware & Sensor Integration

The `Hardware_set_up` module contains utilities for working with sensor-based environmental data.

It includes functionality for:

* Sensor data collection
* Hardware server communication
* Sensor data cleaning
* Database viewing
* Data processing

Example workflow:

```text
Environmental Sensors
        │
        ▼
Hardware Server
        │
        ▼
Sensor Data
        │
        ▼
Data Processing
        │
        ▼
EcoMinds Backend
        │
        ▼
Database + ML Analysis
```

---

## 🔐 Authentication

EcoMinds includes authentication-related routes and interfaces for:

* User registration
* User login
* Authentication management
* Protected application functionality

---

## 📈 Dashboard Modules

The application provides multiple dashboard modules for environmental intelligence:

| Module         | Purpose                                   |
| -------------- | ----------------------------------------- |
| Dashboard      | Central environmental overview            |
| Active Devices | Monitor active connected devices          |
| My Devices     | Manage registered devices                 |
| City Map       | Geographic environmental information      |
| Intelligence   | Environmental insights                    |
| Multi-Risk     | Analyze multiple environmental risks      |
| Parameters     | Monitor environmental parameters          |
| Violations     | Track environmental violations            |
| Alert Log      | View environmental alerts                 |
| Accuracy       | Monitor prediction accuracy               |
| Chatbot        | Interact with the environmental assistant |

---

## 🔮 Future Enhancements

Potential future improvements include:

* Real-time IoT sensor streaming
* Advanced environmental forecasting
* Cloud deployment
* Real-time notification systems
* Improved geospatial visualization
* Automated model retraining
* Advanced anomaly detection
* Mobile application support
* Scalable production database
* Real-time environmental alerting

---

## 🎯 Project Objective

The primary objective of EcoMinds is to combine **environmental monitoring, machine learning, sensor data, and web-based visualization** into a single platform that can help users understand environmental conditions and associated risks.

The platform is designed around the concept:

> **Monitor → Analyze → Predict → Alert → Understand**

---

## 📌 Project Status

EcoMinds is an actively developed environmental intelligence application combining a Flask backend, database services, machine learning models, sensor integration, and an interactive web interface.

---

## 👩‍💻 Author

**Priya Chakane**

GitHub:
https://github.com/PriyaChakane

---

## 📄 License

This project is currently intended for academic and project-development purposes.

A formal open-source license can be added in the future if required.
