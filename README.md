# 🚑 MediRouteX
## An AI-Powered Emergency Response Optimization System for Smart Healthcare Infrastructure

---

## 📌 Overview

MediRouteX is an intelligent emergency response system designed to reduce ambulance response time, optimize routing using traffic-aware graph algorithms, and provide real-time hospital bed availability tracking.

The system integrates:
- AI-based emergency hotspot prediction
- Smart ambulance allocation
- Real-time route optimization
- Hospital resource transparency
- Scalable microservice architecture

---

## 🚨 Problem Statement

Urban emergency response systems suffer from:

- Traffic congestion delays
- Poor ambulance allocation strategies
- Lack of real-time hospital bed visibility
- No predictive planning for high-risk zones

This results in increased emergency response time and avoidable fatalities.

MediRouteX aims to solve these issues using AI, data science, and scalable backend systems.

---

## 🎯 Project Objectives

1. Reduce ambulance response time using smart routing.
2. Provide real-time ICU/Oxygen/Ventilator availability.
3. Predict emergency demand hotspots using machine learning.
4. Build scalable microservice-based backend.
5. Deploy system on cloud infrastructure.

---

## 🏗 System Architecture

### High-Level Architecture

User (Web App - React)
        ↓
API Gateway
        ↓
Microservices:
    - Emergency Service
    - Ambulance Service
    - Hospital Service
    - Routing Service
    - Prediction Service
        ↓
PostgreSQL Database
Redis (Live Location Cache)
        ↓
ML Model Server (Python)
        ↓
AWS Cloud Deployment

---

## 🧠 Core Modules

### 1️⃣ Ambulance Allocation Engine

- Detect nearest available ambulance
- Calculate Estimated Time of Arrival (ETA)
- Assign optimal ambulance

Algorithm:
- Dijkstra / A* Shortest Path
- Priority Queue for optimal selection

---

### 2️⃣ Smart Route Optimization

- Graph-based city map representation
- Nodes = intersections
- Edges = roads
- Edge Weight = distance + traffic multiplier

Advanced:
- A* heuristic-based optimization
- Dynamic traffic simulation

---

### 3️⃣ Real-Time Hospital Bed Dashboard

Hospital Admin Panel:
- Update ICU beds
- Update Oxygen beds
- Update Ventilators

User Interface:
- Display nearest hospital with required facility
- Sort by ETA + availability

---

### 4️⃣ AI Emergency Demand Prediction

Input Features:
- Time of day
- Day of week
- Location
- Historical emergency density
- Weather (optional)

Models:
- Random Forest
- XGBoost
- LSTM (Time Series)

Output:
- Risk score
- Emergency heatmap

---

## 🗄 Database Schema

### Users
- id
- name
- phone
- role

### Ambulances
- id
- latitude
- longitude
- status (available/busy)

### Hospitals
- id
- name
- latitude
- longitude

### Beds
- hospital_id
- icu_available
- oxygen_available
- ventilators_available

### Emergencies
- id
- user_id
- location
- assigned_ambulance
- assigned_hospital
- status
- timestamp

---

## 🛠 Tech Stack

Frontend:
- React
- Mapbox / Leaflet

Backend:
- FastAPI (Python)

Database:
- PostgreSQL
- Redis

AI/ML:
- Scikit-learn
- XGBoost
- Pandas
- NumPy

Cloud:
- AWS EC2
- AWS RDS
- AWS S3

DevOps:
- Docker
- GitHub Actions (CI/CD)

---

## 📂 Project Folder Structure
