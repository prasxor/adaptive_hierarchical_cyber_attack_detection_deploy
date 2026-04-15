# Adaptive Hierarchical Cyber Attack Detection and Localization in Active Distribution Systems

## Overview
This repository contains the implementation of an advanced, adaptive, and hierarchical cyber attack detection system tailored for active distribution networks. The system leverages machine learning methodologies to analyze network datasets and predict specific vectors of cyber attacks in real time, aiding in the swift localization and mitigation of network threats.

## Architecture & Roles
The platform operates on a robust Django backend and provides a seamless, responsive frontend interface powered by Tailwind CSS. It supports two primary actor roles:

1. **Remote User (Analyst/Client)**
   - Secure registration and authentication subsystem.
   - Interface to submit manual network packet payloads and localization metrics (e.g., Datetime, Host, Protocol, Port configs, IP Addressing, Geodata).
   - Real-time prediction and classification of cyber attack types.
   - User profile management.

2. **Service Provider (Administrator)**
   - Administrative dashboard for monitoring registered remote users.
   - Analytics suite featuring CanvasJS to visualize model accuracy, attack type ratios, and dataset anomalies (supporting line, pie, bar, and spline distributions).
   - Centralized control over model training and testing phases.
   - Administrative extraction interfaces for downloading trained analytical datasets.

## Key Features
- **Predictive Analytics**: Evaluate and predict cybersecurity threats based strictly on payload signatures and source localization data.
- **Model Training Visualization**: Dissect performance metrics (accuracy ratios) across different models within the Service Provider portal.
- **Dynamic Data Visualization**: Real-time rendering of network event ratios and prediction aggregations.
- **Segregated Architecture**: Independent application logic handling `Remote_User` and `Service_Provider` namespaces for horizontal scale capabilities.
- **Modern User Interface**: A responsive, Tailwind CSS-driven frontend delivering a streamlined and deeply pragmatic user experience.

## Technology Stack
- **Backend Framework**: Python / Django
- **Frontend / UI**: HTML5, Tailwind CSS
- **Data Visualization**: CanvasJS
- **Database**: Django ORM (SQLite / PostgreSQL integration ready)

## Installation & Setup

### Prerequisites
- Python 3.6 or higher
- pip (Python package installer)

### Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/prasxor/Adaptive-Hierarchical-Cyber-Attack-Detection-and-Localization-in-Active-Distribution-Systems.git
   cd Adaptive-Hierarchical-Cyber-Attack-Detection-and-Localization-in-Active-Distribution-Systems/adaptive_hierarchical_cyber_attack_detection
   ```

2. **Environment Configuration:**
   It is standard practice to run this deployment inside a localized virtual environment.
   ```bash
   python -m venv venv
   
   # On Windows:
   venv\Scripts\activate
   # On Unix/MacOS:
   source venv/bin/activate
   ```

3. **Install Dependencies:**
   Install Django and required architectural libraries.
   ```bash
   pip install django
   # Install corresponding data science extensions if not natively satisfied (e.g., pandas, scikit-learn)
   ```

4. **Database Migrations:**
   Apply backend configurations.
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Launch the Application:**
   ```bash
   python manage.py runserver
   ```
   The application will be accessible at `http://127.0.0.1:8000/`.

## Usage
- **User Portal**: Navigate to the default `/login` route to register or submit network packets for real-time attack detection endpoints.
- **Service Provider Portal**: Navigate to `/serviceproviderlogin` to access the backend monitoring and analytics dashboard.

---
*Developed for research and institutional implementation in active distribution network cybersecurity.*
