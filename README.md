# <p align="center">ARMDET: Alert-based Real-time Monitoring & Detection</p>

> A real-time system that combines weapon detection with automated alerts and data logging. Ideal for enhancing public safety in high-risk environments like campuses, malls, and transit hubs.

---

##  Overview

The increasing number of public threats involving weapons necessitates proactive detection mechanisms. **ARMDET** provides an integrated approach to detecting harmful objects (e.g., knives, guns) in visual feeds and instantly alerting authorities with precise location and timestamp metadata.

## Components

The system is composed of:
-  **YOLOv5-based Detection Engine**
-  **Flask-based API for prediction and response**
-  **Streamlit UI for interactive usage**
-  **Twilio-based SMS Alert System**
-  **Firebase Storage and Realtime Database**

## How to Run

### 1. **Clone the repo**
```bash
git clone https://github.com/yourusername/ARMDET.git
cd ARMDET
```

## Setup Instructions

### 2. **Install Dependencies**
```bash
pip install -r requirements.txt
```

### 3. **Start Flask API**
> Make sure `api.py` is correctly set up with model paths and Twilio keys

**Mac/Linux:**
```bash
export FLASK_APP=api.py
flask run
```

### 4. **Launch Streamlit App**
Open a new terminal and run:
```bash
streamlit run app.py
```

## Supported Modes

| Mode             | Description                                                 |
|------------------|-------------------------------------------------------------|
| **Image Upload** | Detects weapons from uploaded image files                   |
| **Video Upload** | Parses video frames and flags potential threats             |
| **Live Stream**  | Real-time webcam feed detection with automated alerting     |
| **Check Logs**   | Visual interface to view historical detections and metadata |

## Setup Notes

To get started securely and effectively:
- Update your **Twilio credentials** in `twilio_creds.py`
- Place your YOLOv5 models in the `models/` folder
- Ensure `key.json` (Firebase service account) is valid
- Add sensitive files and directories to `.gitignore` to avoid accidental commits

### Example `.gitignore`
```gitignore
*.pyc
__pycache__/
venv/
twilio_creds.py
key.json
models/
```

## 🚧 Upcoming Improvements

- Enhanced **multi-camera support**
- Deploying on **cloud infrastructure** for continuous uptime
- Further **model tuning** for diverse weapon types
- Development of a centralized **dashboard** with log insights and alerts
